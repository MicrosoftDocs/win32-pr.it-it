---
description: La proprietà INSTALLLEVEL è il livello iniziale a cui vengono selezionate le funzionalità &\# 0034;&\# 0034; per l'installazione per impostazione predefinita.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Proprietà INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328432"
---
# <a name="installlevel-property"></a>Proprietà INSTALLLEVEL

La proprietà **INSTALLLEVEL** è il livello iniziale a cui vengono selezionate le funzionalità "on" per l'installazione per impostazione predefinita. Una funzionalità viene installata solo se il valore nel campo livello della tabella delle [funzionalità](feature-table.md) è minore o uguale al valore INSTALLLEVEL corrente. Il livello di installazione per qualsiasi installazione viene specificato dalla proprietà **INSTALLLEVEL** e può essere un integrale compreso tra 1 e 32.767. Per ulteriori informazioni sui livelli di installazione, vedere [tabella delle funzionalità](feature-table.md).

## <a name="default-value"></a>Valore predefinito

Se non viene specificato alcun valore, il livello di installazione viene impostato su 1.

## <a name="remarks"></a>Commenti

È possibile eseguire l'override del livello di installazione specificato dalla proprietà **INSTALLLEVEL** con le proprietà seguenti:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**RIMUOVERE**](remove.md)
-   [**REINSTALL**](reinstall.md)
-   [**PUBBLICIZZARE**](advertise.md)

Ad esempio, l'impostazione di ADDLOCAL = ALL Installa tutte le funzionalità localmente indipendentemente dal valore della proprietà **INSTALLLEVEL** . Se il valore della colonna Level nella [tabella Feature](feature-table.md) è 0, tale funzionalità non viene installata e non viene visualizzata nell'interfaccia utente.

Un amministratore può disabilitare definitivamente una funzionalità applicando una trasformazione di personalizzazione che imposta un valore 0 nella colonna livello per la funzionalità. L'applicazione della trasformazione personalizzazione impedisce l'installazione e la visualizzazione della funzionalità anche se l'utente seleziona un'installazione completa usando l'interfaccia utente o impostando ADDLOCAL su ALL nella riga di comando. Vedere [un esempio di trasformazione della personalizzazione](a-customization-transform-example.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




