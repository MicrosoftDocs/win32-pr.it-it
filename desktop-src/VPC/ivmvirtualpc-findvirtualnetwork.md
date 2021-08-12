---
title: Metodo IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces.h)
description: Recupera un oggetto di rete virtuale che corrisponde al nome richiesto.
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
ms.openlocfilehash: cc8cfb0b8f9b7ee5be7bfb25d7d4cd7ca7b215bcf1824262c576038e75e6ce0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592136"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>Metodo IVMVirtualPC::FindVirtualNetwork

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un oggetto di rete virtuale che corrisponde al nome richiesto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualNetworkName* \[ Pollici\]
</dt> <dd>

Nome della rete virtuale da trovare.

</dd> <dt>

*virtualNetwork* \[ out, retval\]
</dt> <dd>

Puntatore a un nuovo [**oggetto IVMVirtualNetwork**](ivmvirtualnetwork.md) che rappresenta questa rete virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                               | Impossibile trovare la rete virtuale specificata.<br/>                                    |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il *parametro virtualNetwork* è **NULL** o non è possibile trovare la rete virtuale.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Il *parametro virtualNetworkName* non è valido o è una stringa vuota.<br/>               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND) 0X80070002**</dt> <dt></dt> </dl> | Impossibile trovare il file di rete virtuale.<br/>                                         |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Commenti

I nomi di rete virtuale non fanno distinzione tra maiuscole e minuscole, ad esempio "MyNetwork" e "mynetwork" fanno riferimento alla stessa rete virtuale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC è definito come \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

