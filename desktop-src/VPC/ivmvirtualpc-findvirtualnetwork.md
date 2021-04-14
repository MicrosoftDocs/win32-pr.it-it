---
title: Metodo IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera un oggetto rete virtuale che corrisponde al nome richiesto.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Metodo FindVirtualNetwork Virtual PC
- Metodo FindVirtualNetwork Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518471"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>Metodo IVMVirtualPC:: FindVirtualNetwork

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un oggetto rete virtuale che corrisponde al nome richiesto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualNetworkName* \[ in\]
</dt> <dd>

Nome della rete virtuale da trovare.

</dd> <dt>

*virtualNetwork* \[ out, retval\]
</dt> <dd>

Puntatore a un nuovo oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che rappresenta la rete virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                               | La rete virtuale specificata non è stata trovata.<br/>                                    |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro *virtualNetwork* è **null** o non è possibile trovare la rete virtuale.<br/>   |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                 | Il parametro *virtualNetworkName* non è valido o è una stringa vuota.<br/>               |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt> </dl> | Impossibile trovare il file della rete virtuale.<br/>                                         |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |



 

## <a name="remarks"></a>Commenti

I nomi delle reti virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "rete" e "rete" si riferiscono alla stessa rete virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

