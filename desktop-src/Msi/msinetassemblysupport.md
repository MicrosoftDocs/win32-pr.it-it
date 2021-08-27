---
description: La proprietà MsiNetAssemblySupport indica se il computer supporta assembly di runtime in linguaggio comune.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: MsiNetAssemblySupport - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d135fcc9eb301d3624586318fdc0d5dbbc534c5771ee89d4ae625af78b0782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944904"
---
# <a name="msinetassemblysupport-property"></a>MsiNetAssemblySupport - proprietà

La **proprietà MsiNetAssemblySupport** indica se il computer supporta assembly di runtime in linguaggio comune. Nei sistemi che supportano assembly di runtime in linguaggio comune, il programma di installazione imposta il valore di **MsiNetAssemblySupport** sulla versione del file di Fusion.dll. Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta gli assembly di runtime common language. Quando più versioni di Fusion.dll vengono installate side-by-side nel computer dell'utente, questa proprietà viene impostata sulla versione più recente del file Fusion.dll. Ad esempio, se .NET Framework versione 1.0.3705 (Fusion.dll versione 1.0.3705.15) e .NET Framework versione 1.1.4322 (Fusion.dll versione 1.1.4322.314) sono installati side-by-side, La **proprietà MsiNetAssemblySupport** è impostata su 1.1.4322.314. Per altre informazioni, vedere [Assembly](assemblies.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




