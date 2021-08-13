---
description: La proprietà INSTALLLEVEL è il livello iniziale in cui le funzionalità vengono selezionate &\# 0034;ON&0034; per l'installazione per \# impostazione predefinita.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: INSTALLLEVEL - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e349e8d92a2c480866b04a1ca57885ffa1cdb230d8346b357318fa239ead72a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629960"
---
# <a name="installlevel-property"></a>INSTALLLEVEL - proprietà

La **proprietà INSTALLLEVEL** è il livello iniziale in cui le funzionalità vengono selezionate "ON" per l'installazione per impostazione predefinita. Una funzionalità viene installata solo se il valore nel campo Livello della tabella [Funzionalità](feature-table.md) è minore o uguale al valore INSTALLLEVEL corrente. Il livello di installazione per qualsiasi installazione viene specificato dalla **proprietà INSTALLLEVEL** e può essere un integrale da 1 a 32.767. Per altre informazioni sui livelli di installazione, vedere [Tabella delle funzionalità](feature-table.md).

## <a name="default-value"></a>Valore predefinito

Se non viene specificato alcun valore, il livello di installazione viene impostato su 1.

## <a name="remarks"></a>Commenti

Il livello di installazione specificato dalla **proprietà INSTALLLEVEL** può essere sostituito dalle proprietà seguenti:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**Rimuovere**](remove.md)
-   [**REINSTALL**](reinstall.md)
-   [**Pubblicizzare**](advertise.md)

Ad esempio, se si imposta ADDLOCAL=ALL, tutte le funzionalità vengono installate localmente indipendentemente dal valore della **proprietà INSTALLLEVEL.** Se il valore della colonna Level nella [tabella Feature](feature-table.md) è 0, tale funzionalità non viene installata e non viene visualizzata nell'interfaccia utente.

Un amministratore può disabilitare in modo permanente una funzionalità applicando una trasformazione di personalizzazione che imposta 0 nella colonna Livello per tale funzionalità. L'applicazione della trasformazione di personalizzazione impedisce l'installazione e la visualizzazione della funzionalità anche se l'utente seleziona un'installazione completa tramite l'interfaccia utente o impostando ADDLOCAL su ALL nella riga di comando. Vedere [Un esempio di trasformazione di personalizzazione](a-customization-transform-example.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo richiesto da una Windows installer, vedere i Windows Windows di installazione Run-Time requisiti minimi.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




