---
title: Metodo IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces.h)
description: Recupera una matrice di file del disco rigido virtuale noti.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Metodo GetHardDiskFiles Virtual PC
- Metodo GetHardDiskFiles Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 902cd124db27ae65b8f589ded8b2b3188a7e0df67b0ff20071abd04daf5ab894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136574"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a>Metodo IVMVirtualPC::GetHardDiskFiles

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera una matrice di file del disco rigido virtuale noti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inAdditionalSearchPaths* \[ Pollici\]
</dt> <dd>

Questi percorsi verranno cercati insieme ai percorsi impostati nella [**proprietà IVMVirtualPC::SearchPaths.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outHardDiskFileList* \[ out, retval\]
</dt> <dd>

Matrice di stringhe di percorso per i file del disco rigido virtuale trovati nei percorsi di ricerca specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                | Il *parametro outHardDiskFileList* è **NULL.**<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Il *parametro inAdditionalSearchPaths* non è una matrice di stringhe.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0XA0040951</dt> </dl> | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Commenti

I percorsi di ricerca usati per recuperare la matrice di file includeranno quelli impostati in precedenza da [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) oltre a quelli specificati dal *parametro inAdditionalSearchPaths.*

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

 

