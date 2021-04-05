---
title: Metodo IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Recupera un oggetto macchina virtuale che corrisponde alla configurazione richiesta.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Metodo FindVirtualMachine Virtual PC
- Metodo FindVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120786"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a>Metodo IVMVirtualPC:: FindVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un oggetto macchina virtuale che corrisponde alla configurazione richiesta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ConfigurationName* \[ in\]
</dt> <dd>

Nome della macchina virtuale da trovare.

</dd> <dt>

*virtualmachine* \[ out, retval\]
</dt> <dd>

Puntatore a un nuovo oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                           | Impossibile trovare la configurazione specificata.<br/>                                      |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *ConfigurationName* non è valido o *virtualmachine* è **null**.<br/>       |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |



 

## <a name="remarks"></a>Commenti

I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "MyVM" e "MyVM" si riferiscono alla stessa macchina virtuale.

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

 

