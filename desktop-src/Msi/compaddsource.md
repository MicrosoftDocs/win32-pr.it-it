---
description: Il valore della proprietà COMPADDSOURCE è un elenco di GUID del componente della colonna ComponentId della tabella Component, delimitati da virgole, che devono essere installati per l'esecuzione dal supporto di origine.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: COMPADDSOURCE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f68e795a9092892212f41a073a8e5a80945f57be14224e576262c30bba92707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380053"
---
# <a name="compaddsource-property"></a>COMPADDSOURCE - proprietà

Il valore della **proprietà COMPADDSOURCE** è un elenco di GUID del componente della colonna ComponentId della tabella [Component,](component-table.md) delimitati da virgole, che devono essere installati per l'esecuzione dal supporto di origine. Il programma di installazione usa questo valore per determinare le funzionalità impostate per l'installazione per l'esecuzione dall'origine, in base ai componenti specificati. Per ogni ID componente elencato, il programma di installazione esamina tutte le funzionalità collegate (tramite la tabella [FeatureComponents)](featurecomponents-table.md) a tale componente e installa la funzionalità che richiede la quantità minima di spazio su disco da installare. I componenti elencati devono essere presenti nella colonna Componente della [tabella](component-table.md) Componente.

## <a name="remarks"></a>Commenti

Si noti che per i nomi dei componenti viene fatto distinzione tra maiuscole e minuscole. Si noti anche che se il flag di bit LocalOnly è impostato nella colonna Attributi della tabella [Componente](component-table.md) per un componente, il componente viene installato per l'esecuzione in locale.

Il programma di installazione valuta sempre le proprietà seguenti nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Rimuovere**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  [**Pubblicizzare**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  **COMPADDSOURCE**
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
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

 

 




