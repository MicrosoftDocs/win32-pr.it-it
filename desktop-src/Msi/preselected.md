---
description: La proprietà preselezionata indica che le funzionalità sono già state selezionate e che non è necessario visualizzare la finestra di dialogo di selezione. Espressioni condizionali che variano a seconda che le funzionalità siano già installate, usare questo valore.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Proprietà preselezionata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331608"
---
# <a name="preselected-property"></a>Proprietà preselezionata

La proprietà **preselezionata** indica che le funzionalità sono già state selezionate e che non è necessario visualizzare la finestra di dialogo di selezione.

Espressioni condizionali che variano a seconda che le funzionalità siano già installate, usare questo valore. La proprietà, ad esempio, può essere utilizzata per disattivare eventuali finestre di dialogo che coinvolgono le selezioni di funzionalità durante la ripresa di un'installazione sospesa.

Il programma di installazione imposta la proprietà **preselezionata** sul valore "1" durante la ripresa di un'installazione sospesa o quando nella riga di comando viene specificata una delle proprietà seguenti. Se la proprietà **preselezionata** è stata impostata su 1, il programma di installazione non utilizza la [tabella della condizione](condition-table.md) per valutare la selezione delle funzionalità. Le funzionalità vengono installate in base alle proprietà seguenti. Il programma di installazione valuta sempre queste proprietà nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RIMUOVERE**](remove.md)
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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




