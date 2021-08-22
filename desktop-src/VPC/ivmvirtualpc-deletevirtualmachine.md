---
title: Metodo IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces.h)
description: Elimina una configurazione di macchina virtuale.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Metodo DeleteVirtualMachine Virtual PC
- Metodo DeleteVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3471106beeffdfe756ad0793004b68d0a55fd14dda28a9796f4540d2503a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471331"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>Metodo IVMVirtualPC::D eleteVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Elimina una configurazione di macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualMachine* \[ Pollici\]
</dt> <dd>

Puntatore a un [**oggetto IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la configurazione della macchina virtuale da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                           | Impossibile trovare la configurazione specificata.<br/>                                      |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                | Il *parametro virtualMachine* è **NULL.**<br/>                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>                        | La macchina virtuale è in esecuzione.<br/>                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

È possibile eliminare solo le macchine virtuali arrestate. Si noti che qualsiasi stato salvato esistente o i dati dell'unità di annullamento per questa configurazione verranno eliminati in aggiunta al file di configurazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

