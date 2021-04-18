---
description: Il valore della proprietà COMPADDSOURCE è un elenco di GUID del componente della colonna ComponentId della tabella Component, delimitati da virgole, che devono essere installati per l'esecuzione dal supporto di origine.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Proprietà COMPADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326900"
---
# <a name="compaddsource-property"></a>Proprietà COMPADDSOURCE

Il valore della proprietà **COMPADDSOURCE** è un elenco di GUID del componente della colonna ComponentID della tabella [Component](component-table.md) , delimitati da virgole, che devono essere installati per l'esecuzione dal supporto di origine. Il programma di installazione utilizza questo valore per determinare quali funzionalità sono impostate per essere installate per l'esecuzione dall'origine, in base ai componenti specificati. Per ogni ID componente elencato, il programma di installazione esamina tutte le funzionalità collegate (tramite la tabella [FeatureComponents](featurecomponents-table.md) ) a tale componente e installa la funzionalità che richiede la quantità minima di spazio su disco per l'installazione. I componenti elencati devono essere presenti nella colonna componente della tabella dei [componenti](component-table.md) .

## <a name="remarks"></a>Commenti

Si noti che i nomi dei componenti fanno distinzione tra maiuscole e minuscole. Si noti inoltre che se il flag di bit LocalOnly è impostato nella colonna attributi della tabella dei [componenti](component-table.md) per un componente, il componente viene installato per l'esecuzione in locale.

Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RIMUOVERE**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**PUBBLICIZZARE**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  **COMPADDSOURCE**
9.  [**COMPADDDEFAULT**](compadddefault.md)
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

 

 




