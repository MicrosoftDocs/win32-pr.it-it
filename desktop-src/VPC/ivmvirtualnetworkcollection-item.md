---
title: Proprietà IVMVirtualNetworkCollection Item (VPCCOMInterfaces.h)
description: Oggetto IVMVirtualNetwork che corrisponde all'indice specificato.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Proprietà Item Virtual PC
- Proprietà Item Virtual PC, interfaccia IVMVirtualNetworkCollection
- Interfaccia IVMVirtualNetworkCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9133efe93ef5feeb9d8e15862a9d25ea6b14c0de08dd35faa46abc4589fcb21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592319"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a>Proprietà IVMVirtualNetworkCollection::Item

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera [**l'oggetto IVMVirtualNetwork**](ivmvirtualnetwork.md) che corrisponde all'indice specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IVMVirtualNetwork.**](ivmvirtualnetwork.md)

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                                      |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il *parametro virtualNetwork* è **NULL.**<br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                           |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection è definito come 8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> <dt>

[**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

