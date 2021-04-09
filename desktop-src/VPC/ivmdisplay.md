---
title: Interfaccia IVMDisplay (VPCCOMInterfaces. h)
description: Controlla le impostazioni di visualizzazione di una macchina virtuale. L'interfaccia IVMDisplay per una macchina virtuale può essere recuperata usando la proprietà di visualizzazione IVMVirtualMachine.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Interfaccia IVMDisplay Virtual PC
- Interfaccia IVMDisplay Virtual PC, descritta
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
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964599"
---
# <a name="ivmdisplay-interface"></a>Interfaccia IVMDisplay

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controlla le impostazioni di visualizzazione di una macchina virtuale. È possibile recuperare l'interfaccia **IVMDisplay** per una macchina virtuale utilizzando la proprietà [**IVMVirtualMachine::D di riproduzione**](ivmvirtualmachine-display.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMDisplay** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDisplay** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMDisplay** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Recupera una matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.<br/> |
| [**Dimensioni**](ivmdisplay-setdimensions.md)            | Imposta l'altezza e la larghezza della visualizzazione della macchina virtuale, in pixel.<br/>                       |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMDisplay** ha queste proprietà.



| Proprietà                                             | Tipo di accesso          | Descrizione                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Sola lettura<br/> | Indica se il Guest consente le modifiche di risoluzione.<br/>                             |
| [**Altezza**](ivmdisplay-height.md)<br/>       | Sola lettura<br/> | Altezza, in pixel, della visualizzazione della macchina virtuale.<br/>                            |
| [**Anteprima**](ivmdisplay-thumbnail.md)<br/> | Sola lettura<br/> | Matrice di pixel che rappresenta un'immagine di anteprima della schermata della macchina virtuale.<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | Sola lettura<br/> | Modalità video corrente (testo, VGA, SVGA e così via).<br/>                               |
| [**Larghezza**](ivmdisplay-width.md)<br/>         | Sola lettura<br/> | Larghezza, in pixel, dello schermo della macchina virtuale.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

