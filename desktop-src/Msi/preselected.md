---
description: La proprietà Preselezionata indica che le funzionalità sono già state selezionate e che la finestra di dialogo di selezione non deve essere visualizzata. Le espressioni condizionali che dipendono dal fatto che le funzionalità siano già installate usano questo valore.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Proprietà preselezionata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a85f5c3248002fec776e45e9d7ad37550d3e16d7a5d76b098948b571b8c9c546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042321"
---
# <a name="preselected-property"></a>Proprietà preselezionata

La **proprietà Preselezionata** indica che le funzionalità sono già state selezionate e che la finestra di dialogo di selezione non deve essere visualizzata.

Le espressioni condizionali che dipendono dal fatto che le funzionalità siano già installate usano questo valore. Ad esempio, la proprietà può essere usata per eliminare qualsiasi finestra di dialogo che prevede selezioni di funzionalità durante la ripresa di un'installazione sospesa.

Il programma  di installazione imposta la proprietà Preselezionata sul valore "1" durante la ripresa di un'installazione sospesa o quando nella riga di comando viene specificata una delle proprietà seguenti. Se la **proprietà Preselezionata** è stata impostata su 1, il programma di installazione non usa la [tabella Condizione](condition-table.md) per valutare la selezione delle funzionalità. Le funzionalità vengono installate in base alle proprietà seguenti. Il programma di installazione valuta sempre queste proprietà nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




