---
description: Il valore della proprietà ADDSOURCE è un elenco di funzioni delimitate da virgole e deve essere installato per l'esecuzione dall'origine.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Proprietà ADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333578"
---
# <a name="addsource-property"></a>Proprietà ADDSOURCE

Il valore della proprietà **addsource** è un elenco di funzioni delimitate da virgole e deve essere installato per l'esecuzione dall'origine. Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md). Per installare tutte le funzionalità come eseguite dall'origine, usare ADDSOURCE = ALL nella riga di comando. Non immettere ADDSOURCE = ALL nella tabella delle [Proprietà](property-table.md), perché in questo modo viene generato un pacchetto di esecuzione da un'origine che non può essere rimosso correttamente.

## <a name="remarks"></a>Commenti

I nomi delle funzionalità fanno distinzione tra maiuscole e minuscole Se il flag di bit LocalOnly è impostato nella colonna attributi della [tabella dei componenti](component-table.md) per un componente di una funzionalità nell'elenco, tale componente viene installato per l'esecuzione in locale.

Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RIMUOVERE**](remove.md)
3.  **ADDSOURCE**
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**PUBBLICIZZARE**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Ad esempio:

-   Se la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = **funzionalità**, tutte le funzionalità vengono prima impostate su run-local, quindi la **funzionalità** è impostata su Run-from-source.
-   Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la **funzionalità**, First **funzionalità** è impostata su run-local e quindi quando viene valutato addsource = all, tutte le funzionalità (inclusa la **funzionalità**) vengono reimpostate su Run-from-source.

Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




