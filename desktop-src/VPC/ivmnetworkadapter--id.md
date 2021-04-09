---
title: Metodo _ID IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Recupera l'identificatore interno di questa interfaccia di rete.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, metodo _ID
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964345"
---
# <a name="ivmnetworkadapter_id-method"></a>Metodo IVMNetworkAdapter:: \_ ID

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'identificatore interno di questa interfaccia di rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*identificatore* \[ di out\]
</dt> <dd>

Identificatore interno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>           |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl> | Impossibile trovare la macchina virtuale.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Errore sconosciuto durante l'operazione.<br/>  |



 

## <a name="remarks"></a>Commenti

Questo metodo non è utilizzabile dai linguaggi di scripting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

