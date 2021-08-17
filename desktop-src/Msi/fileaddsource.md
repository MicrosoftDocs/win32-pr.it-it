---
description: Il valore della proprietà FILEADDSOURCE indica un elenco di chiavi di file delimitate da virgole che devono essere installate per l'esecuzione dal supporto di origine.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: PROPRIETÀ FILEADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7678c42e683b70fc61e563c57ee234c523078bcdd737bf8f28bc2c05302fbb43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636563"
---
# <a name="fileaddsource-property"></a>PROPRIETÀ FILEADDSOURCE

Il valore della **proprietà FILEADDSOURCE** indica un elenco di chiavi di file delimitate da virgole che devono essere installate per l'esecuzione dal supporto di origine. Per ogni chiave di file nell'elenco, il programma di installazione determina il componente che controlla il file, quindi esamina tutte le funzionalità collegate a tale componente dalla tabella [FeatureComponents](featurecomponents-table.md) e installa la funzionalità che richiede la quantità minima di spazio su disco. Le chiavi di file nell'elenco devono essere presenti nella colonna File della [tabella File.](file-table.md)

## <a name="remarks"></a>Commenti

Si noti che per i nomi delle chiavi di file viene fatto distinzione tra maiuscole e minuscole. Si noti anche che se il flag di bit LocalOnly è impostato nella colonna Attributi della tabella [Componente](component-table.md) per un componente, il componente viene installato per l'esecuzione in locale.

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
11. **FILEADDSOURCE**
12. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 




