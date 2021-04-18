---
description: Il valore della proprietà COMPADDDEFAULT è un elenco di GUID del componente della colonna ComponentId della tabella Component, delimitati da virgole, che vengono installati nella configurazione predefinita.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: Proprietà COMPADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326901"
---
# <a name="compadddefault-property"></a>Proprietà COMPADDDEFAULT

Il valore della proprietà **COMPADDDEFAULT** è un elenco di GUID del componente della colonna ComponentID della [tabella Component](component-table.md), delimitati da virgole, che vengono installati nella configurazione predefinita. Per ogni ID componente nell'elenco, il programma di installazione installa la funzionalità che richiede lo spazio minimo su disco. Gli ID componente nell'elenco devono essere presenti nella colonna ComponentId della [tabella Component](component-table.md). Una funzionalità viene installata nello stesso stato di installazione come se l'utente avesse richiesto un'installazione su richiesta della funzionalità. Lo stato è determinato dai bit impostati per la funzionalità nella colonna attributi della [tabella delle funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna attributi della tabella dei componenti.

## <a name="remarks"></a>Commenti

Si noti che se il flag di bit SourceOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione dall'origine.

Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RIMUOVERE**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**PUBBLICIZZARE**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  **COMPADDDEFAULT**
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 




