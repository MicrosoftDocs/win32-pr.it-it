---
title: Metodo IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Recupera una matrice di file di configurazione della macchina virtuale noti.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Metodo GetVirtualMachineFiles Virtual PC
- Metodo GetVirtualMachineFiles Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341223"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>Metodo IVMVirtualPC:: GetVirtualMachineFiles

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matrice di file di configurazione della macchina virtuale noti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inAdditionalSearchPaths* \[ in\]
</dt> <dd>

Questi percorsi verranno cercati insieme ai percorsi impostati nelle proprietà [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .

</dd> <dt>

*inExcludedRegisteredVMs* \[ in\]
</dt> <dd>

**True** se le macchine virtuali registrate devono essere escluse dalla matrice restituita nel parametro *outVirtualMachineFileList* e **false** in caso contrario.

</dd> <dt>

*outVirtualMachineFileList* \[ out, retval\]
</dt> <dd>

Matrice di stringhe di percorso per i file di configurazione della macchina virtuale trovati nei percorsi di ricerca specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *outVirtualMachineFileList* è **null**.<br/>                               |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                             | Il parametro *inAdditionalSearchPaths* non è una matrice di stringhe.<br/>                  |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |



 

## <a name="remarks"></a>Commenti

I percorsi di ricerca usati per recuperare la matrice di file di configurazione includeranno quelli impostati in precedenza da [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) , oltre a quelli specificati dal parametro *inAdditionalSearchPaths* .

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

 

