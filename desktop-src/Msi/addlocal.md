---
description: Il valore della proprietà ADDLOCAL è un elenco di funzionalità delimitate da virgole e che devono essere installate in locale.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82ca86fabd1f90c55c1c3dbf4704a89480a9b23a19f943aca3fd53c1f9065270
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822011"
---
# <a name="addlocal-property"></a>ADDLOCAL - proprietà

Il valore della **proprietà ADDLOCAL** è un elenco di funzionalità delimitate da virgole e che devono essere installate in locale. Le funzionalità devono essere presenti nella colonna Funzionalità della [tabella delle funzionalità](feature-table.md). Per installare tutte le funzionalità in locale, usare ADDLOCAL=ALL nella riga di comando. Non immettere ADDLOCAL=ALL nella [tabella](property-table.md)delle proprietà perché viene generato un pacchetto installato localmente che non può essere rimosso correttamente.

## <a name="remarks"></a>Commenti

Per i nomi delle funzionalità viene fatto distinzione tra maiuscole e minuscole. Se il flag di bit SourceOnly è [](component-table.md) impostato nella colonna Attributi della tabella dei componenti per un componente di una funzionalità nell'elenco, tale componente viene installato come eseguito dall'origine.

Il programma di installazione valuta sempre le proprietà seguenti nell'ordine seguente:

1.  **ADDLOCAL**
2.  [**Rimuovere**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**Pubblicizzare**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Esempio:

-   Se la riga di comando specifica: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, tutte le funzionalità vengono prima impostate su run-local e quindi **MyFeature** su run-from-source.
-   Se la riga di comando è: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, prima **MyFeature** è impostato su run-local e quindi quando viene valutato ADDSOURCE=ALL, tutte le funzionalità (inclusa **MyFeature**) vengono reimpostate su run-from-source.

Il programma [](preselected.md) di installazione imposta la proprietà preselezionata sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà precedenti viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




