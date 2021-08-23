---
title: Metodo IVMVirtualPC GetHardDisk (VPCCOMInterfaces.h)
description: Recupera un oggetto corrispondente a un file di immagine disco esistente.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Metodo GetHardDisk Virtual PC
- Metodo GetHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc57085662c62951032837db178888bac5cb4407b11d7777d2f165f7b9c5a100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136584"
---
# <a name="ivmvirtualpcgetharddisk-method"></a>Metodo IVMVirtualPC::GetHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un oggetto corrispondente a un file di immagine disco esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*imagePath* \[ Pollici\]
</dt> <dd>

Percorso completo di un file di immagine disco esistente.

</dd> <dt>

*hardDisk* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMHardDisk**](ivmharddisk.md) corrispondente a questa immagine disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                         |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il *parametro imagePath* *o hardDisk* è **NULL.**<br/>                                                                  |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO)**</dt> <dt>0X80070002</dt> </dl> | Il sistema non riesce a trovare il file specificato dal *parametro imagePath.*<br/>                                               |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(PERCORSO \_ ERRORE NON \_ \_ TROVATO) 0X80070003**</dt> <dt></dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro imagePath.*<br/>                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro imagePath* contiene un carattere non valido (uno di " \* ?:<>/ \| "").<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Il *parametro imagePath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro imagePath* è troppo lungo. La lunghezza del percorso deve essere inferiore a 260 caratteri.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                     |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0XA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                  |



 

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

 

