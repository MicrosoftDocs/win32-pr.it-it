---
description: La proprietà MsiNetAssemblySupport indica se il computer supporta gli assembly Common Language Runtime.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Proprietà MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326771"
---
# <a name="msinetassemblysupport-property"></a>Proprietà MsiNetAssemblySupport

La proprietà **MsiNetAssemblySupport** indica se il computer supporta gli assembly Common Language Runtime. Nei sistemi che supportano gli assembly di runtime del linguaggio comune, il programma di installazione imposta il valore di **MsiNetAssemblySupport** sulla versione del file di Fusion.dll. Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta gli assembly Common Language Runtime. Quando più versioni di Fusion.dll vengono installate side-by-side nel computer dell'utente, questa proprietà viene impostata sulla versione più recente del file di Fusion.dll. Se, ad esempio, .NET Framework versione 1.0.3705 (Fusion.dll versione 1.0.3705.15) e .NET Framework versione 1.1.4322 (Fusion.dll versione 1.1.4322.314) vengono installate side-by-Side, la proprietà **MsiNetAssemblySupport** è impostata su 1.1.4322.314. Per ulteriori informazioni, vedere [assembly](assemblies.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




