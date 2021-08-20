---
title: Metodo IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces.h)
description: Recupera il tipo di un file di immagine disco floppy esistente.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Metodo GetFloppyDiskImageType Virtual PC
- Metodo GetFloppyDiskImageType Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891e07da259acc8e2efa759d636ac203654700785586a20f879cf75165ab318e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122330"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a>Metodo IVMVirtualPC::GetFloppyDiskImageType

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il tipo di un file di immagine disco floppy esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*imagePath* \[ Pollici\]
</dt> <dd>

Percorso completo del file di immagine del disco.

</dd> <dt>

*imageType* \[ out, retval\]
</dt> <dd>

Tipo di immagine disco. Per un elenco di valori, vedere [**VMFloppyDiskImageType.**](vmfloppydiskimagetype.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                         |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il *parametro imagePath* *o imageType* è **NULL.**<br/>                                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0x80070002</dt> </dl> | Il sistema non riesce a trovare il file specificato dal *parametro imagePath.*<br/>                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro imagePath.*<br/>                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro imagePath* contiene un carattere non valido (uno tra " \* ?:<>/ \| "").<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Il *parametro imagePath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro imagePath* è troppo lungo. La lunghezza del percorso deve essere minore di 260 caratteri.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                            | Il file specificato da *imagePath non* è un'immagine floppy o si è verificato un errore imprevisto.<br/>                         |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

