---
description: Il valore della proprietà FILEADDDEFAULT è un elenco di chiavi file delimitate da virgole installate nella configurazione predefinita.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: PROPRIETÀ FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa5692cbba5b00aff6c3cbdef66e33420b4b135d0c3dfa13d9ae6e2255e5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828951"
---
# <a name="fileadddefault-property"></a>PROPRIETÀ FILEADDDEFAULT

Il valore della **proprietà FILEADDDEFAULT** è un elenco di chiavi file delimitate da virgole installate nella configurazione predefinita. Per ogni chiave di file nell'elenco, il programma di installazione determina il componente che controlla tale file e installa la funzionalità che richiede meno spazio su disco. Le chiavi di file nell'elenco devono essere presenti nella colonna File della [tabella File.](file-table.md) Una funzionalità viene installata nello stesso stato di installazione di se l'utente avesse richiesto un'installazione su richiesta della funzionalità. Lo stato è determinato dai bit impostati per la funzionalità nella colonna Attributi della tabella [Funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna Attributi della tabella [Componente](component-table.md).

## <a name="remarks"></a>Commenti

Si noti che per i nomi delle chiavi di file viene fatto distinzione tra maiuscole e minuscole. Si noti anche che se il flag di bit SourceOnly è impostato nella colonna Attributi della tabella [Componente](component-table.md) per un componente, il componente viene installato per l'esecuzione dall'origine.

Il programma di installazione valuta sempre le proprietà seguenti nell'ordine seguente.

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
12. **FILEADDDEFAULT**

Ad esempio, se la riga di comando specifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, tutte le funzionalità vengono prima impostate su run-local e quindi MyFeature su run-from-source. Se la riga di comando è: ADDSOURCE=ALL, ADDLOCAL=MyFeature, prima MyFeature è impostata su run-local e quindi quando si valuta ADDSOURCE=ALL, tutte le funzionalità (inclusa MyFeature) vengono reimpostate su run-from-source.

Il programma [](preselected.md) di installazione imposta la proprietà Preselezionata sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà precedenti viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




