---
title: Metodo IVMVirtualPC GetFloppyDiskFiles (VPCCOMInterfaces. h)
description: Recupera una matrice di file di dischi floppy virtuali noti.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- Metodo GetFloppyDiskFiles Virtual PC
- Metodo GetFloppyDiskFiles Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetFloppyDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9759a3b909bb4f4ac179c166635185a701a8a16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743442"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a>Metodo IVMVirtualPC:: GetFloppyDiskFiles

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera una matrice di file di dischi floppy virtuali noti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inAdditionalSearchPaths* \[ in\]
</dt> <dd>

Questi percorsi verranno cercati insieme ai percorsi impostati nella proprietà [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .

</dd> <dt>

*outFloppyDiskFileList* \[ out, retval\]
</dt> <dd>

Matrice di file di dischi floppy virtuali trovati nei percorsi di ricerca specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *outFloppyDiskFileList* è **null**.<br/>                                   |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                             | Il parametro *inAdditionalSearchPaths* non è una matrice di stringhe.<br/>                  |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |



 

## <a name="remarks"></a>Commenti

I percorsi di ricerca usati per recuperare la matrice di file includeranno quelli impostati in precedenza da [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) , oltre a quelli specificati dal parametro *inAdditionalSearchPaths* e dal percorso del programma di installazione per il modulo Integration Components.

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

 

