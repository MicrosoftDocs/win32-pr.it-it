---
description: Il valore della proprietà ADDSOURCE è un elenco di funzionalità delimitate da virgole che devono essere installate per l'esecuzione dall'origine.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: AddSOURCE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420ca53a96ddeb379a7e021db2c45157861acfb62d066cadfc7a163db7fbc307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078161"
---
# <a name="addsource-property"></a>AddSOURCE - proprietà

Il valore della **proprietà ADDSOURCE** è un elenco di funzionalità delimitate da virgole che devono essere installate per l'esecuzione dall'origine. Le funzionalità devono essere presenti nella colonna Funzionalità della [tabella delle funzionalità](feature-table.md). Per installare tutte le funzionalità come eseguite dall'origine, usare ADDSOURCE=ALL nella riga di comando. Non immettere ADDSOURCE=ALL nella tabella delle proprietà [perché](property-table.md)viene generato un pacchetto run-from-source che non può essere rimosso correttamente.

## <a name="remarks"></a>Commenti

Per i nomi delle funzionalità viene fatto distinzione tra maiuscole e minuscole. Se il flag di bit LocalOnly è [](component-table.md) impostato nella colonna Attributi della tabella dei componenti per un componente di una funzionalità nell'elenco, tale componente viene installato per l'esecuzione locale.

Il programma di installazione valuta sempre le proprietà seguenti nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Rimuovere**](remove.md)
3.  **ADDSOURCE**
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

 

 




