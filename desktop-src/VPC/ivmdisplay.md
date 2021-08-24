---
title: Interfaccia IVMDisplay (VPCCOMInterfaces.h)
description: Controlla le impostazioni di visualizzazione di una macchina virtuale. L'interfaccia IVMDisplay per una macchina virtuale può essere recuperata usando la proprietà IVMVirtualMachine Display.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Interfaccia IVMDisplay Virtual PC
- Interfaccia IVMDisplay Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6239747477cdddf0ecbcf3acac90e33e61c0f5f4c9dd327b80eb6a33cb113c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654141"
---
# <a name="ivmdisplay-interface"></a>Interfaccia IVMDisplay

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controlla le impostazioni di visualizzazione di una macchina virtuale. **L'interfaccia IVMDisplay** per una macchina virtuale può essere recuperata usando la proprietà [**IVMVirtualMachine::D isplay.**](ivmvirtualmachine-display.md)

## <a name="members"></a>Membri

**L'interfaccia IVMDisplay** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDisplay** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMDisplay** include questi metodi.



| Metodo                                                       | Descrizione                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Recupera una matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale.<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | Imposta l'altezza e la larghezza della visualizzazione della macchina virtuale, in pixel.<br/>                       |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IVMDisplay** ha queste proprietà.



| Proprietà                                             | Tipo di accesso          | Descrizione                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Sola lettura<br/> | Indica se guest consente modifiche alla risoluzione.<br/>                             |
| [**Altezza**](ivmdisplay-height.md)<br/>       | Sola lettura<br/> | Altezza della visualizzazione della macchina virtuale, in pixel.<br/>                            |
| [**Anteprima**](ivmdisplay-thumbnail.md)<br/> | Sola lettura<br/> | Matrice di pixel che rappresenta un'immagine di anteprima dello schermo della macchina virtuale.<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | Sola lettura<br/> | Modalità video corrente (testo, VGA, SVGA e così via).<br/>                               |
| [**Larghezza**](ivmdisplay-width.md)<br/>         | Sola lettura<br/> | Larghezza in pixel dello schermo della macchina virtuale.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay è definito come \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

