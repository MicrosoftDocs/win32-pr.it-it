---
description: Il valore della proprietà ADVERTISE è un elenco di funzionalità delimitate da virgole che devono essere annunciate.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: PROPRIETÀ ADVERTISE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da43d291b64ed10c1ae5321a766eca6cab9c4423a26625aacd92e9591d2e3f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381600"
---
# <a name="advertise-property"></a>PROPRIETÀ ADVERTISE

Il valore della **proprietà ADVERTISE** è un elenco di funzionalità delimitate da virgole che devono essere annunciate. Le funzionalità devono essere presenti nella colonna Funzionalità della [tabella](feature-table.md) Funzionalità. Per installare tutte le funzionalità annunciate, usare ADVERTISE=ALL nella riga di comando. Non immettere ADVERTISE=ALL nella tabella [Proprietà](property-table.md) perché viene generato un pacchetto annunciato che non può essere installato o rimosso.

## <a name="remarks"></a>Commenti

Si noti che per i nomi delle funzionalità viene fatto distinzione tra maiuscole e minuscole.

Il programma di installazione valuta sempre le proprietà seguenti nell'ordine seguente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Rimuovere**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALL**](reinstall.md)
6.  **Pubblicizzare**
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
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

 

 




