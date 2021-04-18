---
description: Il valore della proprietà ADDDEFAULT è un elenco di funzionalità delimitate da virgole, che devono essere installate nella configurazione predefinita.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Proprietà ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326053"
---
# <a name="adddefault-property"></a>Proprietà ADDDEFAULT

Il valore della proprietà **AddDefault** è un elenco di funzionalità delimitate da virgole, che devono essere installate nella configurazione predefinita. Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità.](feature-table.md) Per installare tutte le funzionalità nelle configurazioni predefinite, usare ADDDEFAULT = ALL nella riga di comando.

Una funzionalità elencata nella proprietà **AddDefault** viene installata nello stesso stato di installazione di se l'utente ha richiesto un'installazione su richiesta della funzionalità. Lo stato è determinato dai bit impostati per la funzionalità nella colonna attributi della [tabella delle funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna attributi della [tabella dei componenti](component-table.md).

## <a name="remarks"></a>Commenti

I nomi delle funzionalità fanno distinzione tra maiuscole e minuscole

Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RIMUOVERE**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**REINSTALL**](reinstall.md)
6.  [**PUBBLICIZZARE**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Ad esempio:

-   Se la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la **funzionalità** è impostata su Run-from-source.
-   Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First **funzionalità** è impostata su run-local e quindi quando viene valutato addsource = all, tutte le funzionalità (inclusa la **funzionalità**) vengono reimpostate su Run-from-source.

Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




