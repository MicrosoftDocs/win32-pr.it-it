---
description: Il valore della proprietà FILEADDDEFAULT è un elenco di chiavi di file delimitate da virgole installate nella configurazione predefinita.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: Proprietà FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324780"
---
# <a name="fileadddefault-property"></a>Proprietà FILEADDDEFAULT

Il valore della proprietà **FILEADDDEFAULT** è un elenco di chiavi di file delimitate da virgole installate nella configurazione predefinita. Per ogni chiave file nell'elenco, il programma di installazione determina il componente che controlla il file e installa la funzionalità che richiede lo spazio su disco minimo. Le chiavi del file nell'elenco devono essere presenti nella colonna file della tabella [file](file-table.md) . Una funzionalità viene installata nello stesso stato di installazione come se l'utente avesse richiesto un'installazione su richiesta della funzionalità. Lo stato è determinato dai bit impostati per la funzionalità nella colonna attributi della [tabella delle funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna attributi della [tabella dei componenti](component-table.md).

## <a name="remarks"></a>Commenti

Si noti che i nomi delle chiavi del file fanno distinzione tra maiuscole e minuscole. Si noti inoltre che se il flag di bit SourceOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione dall'origine.

Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente.

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
12. **FILEADDDEFAULT**

Se, ad esempio, la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = la funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la funzionalità è impostata su Run-from-source. Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First funzionalità è impostata su run-local e quindi quando viene valutato ADDSOURCE = ALL, tutte le funzionalità (inclusa la funzionalità) vengono reimpostate su Run-from-source.

Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




