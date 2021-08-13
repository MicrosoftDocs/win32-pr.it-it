---
description: Il valore della proprietà ADDDEFAULT è un elenco di funzionalità delimitate da virgole, che devono essere installate nella configurazione predefinita.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: ADDDEFAULT - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e854df38b58a19f41f98cf1f96657dafdda0c4134c7085c50b4c9c4528b3164e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639705"
---
# <a name="adddefault-property"></a>ADDDEFAULT - proprietà

Il valore della **proprietà ADDDEFAULT** è un elenco di funzionalità delimitate da virgole, che devono essere installate nella configurazione predefinita. Le funzionalità devono essere presenti nella colonna Funzionalità della [tabella delle funzionalità.](feature-table.md) Per installare tutte le funzionalità nelle configurazioni predefinite, usare ADDDEFAULT=ALL nella riga di comando.

Una funzionalità elencata nella **proprietà ADDDEFAULT** viene installata nello stesso stato di installazione di se l'utente ha richiesto un'installazione su richiesta della funzionalità. Lo stato è determinato dai bit impostati per la funzionalità [](feature-table.md)nella colonna Attributi della tabella delle funzionalità e dai bit impostati per i componenti della funzionalità nella colonna Attributi della tabella [dei componenti](component-table.md).

## <a name="remarks"></a>Commenti

Per i nomi delle funzionalità viene fatto distinzione tra maiuscole e minuscole.

Il programma di installazione valuta sempre le proprietà seguenti nell'ordine seguente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Rimuovere**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**REINSTALL**](reinstall.md)
6.  [**Pubblicizzare**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Esempio:

-   Se la riga di comando specifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, tutte le funzionalità vengono prima impostate su run-local e quindi **MyFeature** su run-from-source.
-   Se la riga di comando è: ADDSOURCE=ALL, ADDLOCAL=MyFeature, **prima MyFeature** è impostata su run-local e quindi quando si valuta ADDSOURCE=ALL, tutte le funzionalità (inclusa **MyFeature**) vengono reimpostate su run-from-source.

Il programma [](preselected.md) di installazione imposta la proprietà Preselezionata sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà precedenti viene specificata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo richiesto da una Windows installer, vedere i Windows Windows di installazione Run-Time requisiti minimi.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




