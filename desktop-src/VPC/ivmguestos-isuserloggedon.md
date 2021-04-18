---
title: Metodo IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Determina se la sessione richiesta è presente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Metodo IsUserLoggedOn Virtual PC
- Metodo IsUserLoggedOn Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301048"
---
# <a name="ivmguestosisuserloggedon-method"></a>Metodo IVMGuestOS:: IsUserLoggedOn

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se la sessione richiesta è presente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inRailSession* \[ in\]
</dt> <dd>

Impostare su 0 per una sessione binaria o 1 per una sessione RDP.

</dd> <dt>

*outSessionPresent* \[ out, retval\]
</dt> <dd>

Impostare su **Variant \_ true** se la sessione è presente e **Variant \_ false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | L'operazione è stata completata.<br/>                                   |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                               | Il parametro è **null**.<br/>                                      |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                            | Il parametro *outSessionPresent* non è valido o è **null**.<br/>  |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                       | Si è verificato un errore imprevisto.<br/>                               |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt> </dl> | La memoria disponibile non è sufficiente per completare la richiesta.<br/>  |
| <dl> <dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt> </dl>                        | L'operazione non è stata completata in modo tempestivo.<br/>              |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                  | Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.<br/>    |
| <dl> <dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt> </dl>    | La funzionalità componenti di integrazione non è installata in questa macchina virtuale.<br/> |
| <dl> <dt>**Macchina virtuale \_ 0xA00400507 \_ macchina virtuale E \_ sospesa**</dt> <dt></dt> </dl>                       | La macchina virtuale è sospesa.<br/>                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

