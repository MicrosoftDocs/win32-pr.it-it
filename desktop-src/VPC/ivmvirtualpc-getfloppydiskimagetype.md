---
title: Metodo IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Recupera il tipo di un file di immagine del disco floppy esistente.
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
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121346"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a>Metodo IVMVirtualPC:: GetFloppyDiskImageType

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il tipo di un file di immagine del disco floppy esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*imagePath* \[ in\]
</dt> <dd>

Percorso completo del file di immagine del disco.

</dd> <dt>

*ImageType* \[ out, retval\]
</dt> <dd>

Tipo di immagine disco. Per un elenco di valori, vedere [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                         |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro *imagePath* o *ImageType* è **null**.<br/>                                                                 |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt> </dl> | Il sistema non è in grado di trovare il file specificato dal parametro *imagePath* .<br/>                                               |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* .<br/>                                               |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>    | Il parametro *imagePath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").<br/>                                  |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *imagePath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                          |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal parametro *imagePath* è troppo lungo. La lunghezza del percorso deve essere inferiore a 260 caratteri.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Il file specificato da *imagePath* non è un'immagine floppy oppure si è verificato un errore imprevisto.<br/>                         |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/>                                  |



 

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

 

