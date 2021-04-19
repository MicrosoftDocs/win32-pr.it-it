---
description: Il valore della proprietà REMOVE è un elenco di funzioni delimitate da virgole da rimuovere.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332606"
---
# <a name="remove-property"></a>REMOVE - proprietà

Il valore della proprietà **Remove** è un elenco di funzioni delimitate da virgole da rimuovere. Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità](feature-table.md). Si noti che se si usa REMOVE = ALL nella riga di comando, il programma di installazione rimuove tutte le funzionalità con un livello di installazione maggiore di 0. In questo caso, il programma di installazione non rimuove le funzionalità che hanno un livello di installazione pari a 0. Per ulteriori informazioni sul livello di installazione delle funzionalità, vedere [tabella delle funzionalità](feature-table.md).

## <a name="remarks"></a>Commenti

Per determinare se un prodotto è stato impostato per la disinstallazione completa, l'autore di un pacchetto può utilizzare un'espressione condizionale per verificare se REMOVE = ALL. Si noti che se il prodotto viene rimosso impostando la funzionalità principale su assente, la proprietà **Remove** potrebbe non essere uguale a All fino a dopo l' [azione InstallValidate](installvalidate-action.md). Ciò significa che qualsiasi azione personalizzata che dipende da REMOVE = ALL deve essere sequenziata dopo InstallValidate. Per ulteriori informazioni, vedere anche [condizionare le azioni da eseguire durante la rimozione](conditioning-actions-to-run-during-removal.md). Si noti che i nomi delle funzionalità fanno distinzione tra maiuscole e minuscole.

Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  **RIMUOVERE**
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**PUBBLICIZZARE**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Se, ad esempio, nella riga di comando viene specificato ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source. Se la riga di comando è ADDSOURCE = ALL, ADDLOCAL = la funzionalità, la prima funzionalità è impostata su run-local, quindi, quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.

Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




