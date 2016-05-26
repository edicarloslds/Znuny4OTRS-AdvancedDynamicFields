# Consultant Helfer

Viele Aufgaben die bei einer Einrichtung oder Aktualisierung eines Kundensystems vorgenommen werden müssen sind aufgrund diverser Limitierungen sehr mühsam. Diese Erweiterung soll die Arbeiten an Kundensystemen erleichtern.

## Verwaltung von Dashboard DefaultColumns

Um im OTRS Standard Ticket Attribute in allen Dashboard SysConfig Konfigurationen hinzuzufügen, bearbeiten oder zu löschen muss jeder Konfigurationseintrag manuell über die SysConfig Oberfläche angepasst werden. Das neue OTRS Konsolenkommando "Znuny4OTRS::DashboardColumn::Add" erleichtert diese Arbeit, indem das übergebene Ticket Attribut in allen entsprechenden Dashboard Konfigurationen mit dem übergebenen Wert gesetzt wird.

Die Hilfe kann wie folgt ausgegeben werden:
```
./bin/otrs.Console.pl Znuny4OTRS::DashboardColumn::Add
```

Beispielaufruf:
```
./bin/otrs.Console.pl Znuny4OTRS::DashboardColumn::Add DynamicField_Test 2
```

Zum Löschen kann das Konsolenkommando "Znuny4OTRS::DashboardColumn::Remove" analog verwendet werden.

Die Hilfe kann wie folgt ausgegeben werden:
```
./bin/otrs.Console.pl Znuny4OTRS::DashboardColumn::Remove
```

Beispielaufruf:
```
./bin/otrs.Console.pl Znuny4OTRS::DashboardColumn::Remove DynamicField_Test
```

## Verwaltung von DynamicFields im Frontend

Um im OTRS Standard dynamische Felder in allen möglichen Oberflächen hinzuzufügen, bearbeiten oder zu löschen muss jeder Konfigurationseintrag manuell über die SysConfig Oberfläche angepasst werden. Das neue OTRS Konsolenkommando "Znuny4OTRS::DynamicFieldScreen::Add" erleichtert diese Arbeit, indem das übergebene dynamische Felder in allen entsprechenden Oberflächen mit dem übergebenen Wert gesetzt wird.
Es können bestimmte / mehrere Oberflächen mit dem Parameter screen gesetzten werden.
Default werden alle mögliche Oberflächen verwendet.

Die Hilfe kann wie folgt ausgegeben werden:
```
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Add
```

Die möglichen Screens und dynamischen Felder können wie folgt ausgegeben werden:
```
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Add --values
```

Beispielaufruf:
```
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Add --dynamicfield=FieldName --dynamicfield=FieldName2 --state 1

Screen ist optional
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Add --dynamicfield=FieldName --dynamicfield=FieldName2 --state 1 --screen=AgentTicketNote --screen=AgentTicketZoom
```



Zum Löschen kann das Konsolenkommando "Znuny4OTRS::DynamicFieldScreen::Remove" analog verwendet werden.

Die Hilfe kann wie folgt ausgegeben werden:
```
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Remove
```

Die möglichen Screens und dynamischen Felder können wie folgt ausgegeben werden:
```
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Remove --values
```

Beispielaufruf:
```
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Remove --dynamicfield=FieldName --dynamicfield=FieldName2

Screen ist optional
./bin/otrs.Console.pl Znuny4OTRS::DynamicFieldScreen::Remove --dynamicfield=FieldName --dynamicfield=FieldName2 --screen=AgentTicketNote --screen=AgentTicketZoom

```
