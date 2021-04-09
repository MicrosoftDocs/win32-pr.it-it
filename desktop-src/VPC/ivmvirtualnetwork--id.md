---
title: Metodo _ID IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera l'identificatore interno della rete virtuale.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMVirtualNetwork
- Interfaccia IVMVirtualNetwork Virtual PC, metodo _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048663"
---
# <a name="ivmvirtualnetwork_id-method"></a>Metodo IVMVirtualNetwork:: \_ ID

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'identificatore interno della rete virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualNetworkID* \[ out\]
</dt> <dd>

Identificatore della rete virtuale. L'identificatore per la rete virtuale NAT (Shared Networking) è 01010101010101010101010101010101.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



 

## <a name="remarks"></a>Commenti

Questa proprietà non è utilizzabile dai linguaggi di scripting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

