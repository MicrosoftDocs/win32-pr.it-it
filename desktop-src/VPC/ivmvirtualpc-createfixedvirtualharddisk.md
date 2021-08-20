---
title: Metodo IVMVirtualPC CreateFixedVirtualHardDisk (VPCCOMInterfaces.h)
description: Crea un disco rigido virtuale di dimensioni fisse.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Metodo CreateFixedVirtualHardDisk virtual PC
- Metodo CreateFixedVirtualHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateFixedVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342fe173b8948fe1f445d4cf626602347fa845c914c6525d592069191062b3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056599"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a>Metodo IVMVirtualPC::CreateFixedVirtualHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Crea un disco rigido virtuale di dimensioni fisse.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*imagePath* \[ Pollici\]
</dt> <dd>

Percorso completo del nuovo file di immagine del disco. Se non esiste, verrà creata la cartella che la contiene.

</dd> <dt>

*size* \[ Pollici\]
</dt> <dd>

Dimensioni, in megabyte, dell'immagine. La dimensione massima è 2.088.960 MB (2040 GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia della creazione dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Un parametro è **NULL.**<br/>                                                                                                                             |
| <dl> <dt>**E \_ InvalidARG**</dt> <dt>0x80000003</dt> </dl>                                 | Il *parametro size* è minore o uguale a 0.<br/>                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro imagePath.*<br/>                                                                              |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0x8007000f</dt> </dl>   | Il file specificato dal *parametro imagePath* si trova in un CD-ROM o DVD-ROM.<br/>                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro imagePath* contiene un carattere non valido (uno tra " \* ?:<>/ \| "").<br/>                                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Entrambi i *parametri imagePath* specificano un percorso vuoto o relativo. Almeno uno dei parametri deve essere un percorso assoluto.<br/>                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro imagePath* è troppo lungo. La lunghezza del percorso deve essere minore di **MAX \_ PATH** (260) caratteri.<br/>                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | Il file a cui fa riferimento *il parametro imagePath* esiste già.<br/>                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | L'immagine del disco rigido virtuale a espansione dinamica richiede almeno 8 MB di spazio disponibile nel volume host.<br/>                                                       |
| <dl> <dt>**Macchina virtuale \_ E \_ DIMENSIONI \_ \_ DELL'IMMAGINE TROPPO \_ GRANDI**</dt> <dt>0XA0040683</dt> </dl>                | Il *parametro size* deve essere minore di 2.088.960 MB. Se il formato è FAT16, il *parametro size* deve essere minore di 2000 MB.<br/>                    |
| <dl> <dt>**Macchina virtuale \_ E \_ DIMENSIONI \_ \_ DELL'IMMAGINE TROPPO PICCOLE \_ 0XA0040684**</dt> <dt></dt> </dl>                | Le immagini di dischi rigidi virtuali formattati non formattati e FAT16 devono essere di almeno 3 MB. Le immagini del disco rigido virtuale in formato FAT32 devono essere di almeno 514 MB.<br/>    |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE TOO LARGE FOR \_ \_ \_ \_ VOLUME**</dt> <dt>0xA0040679</dt> </dl>          | Il volume host non può supportare un file di queste dimensioni. Le dimensioni massime dei file per un volume FAT32 sono di 4 GB. Le dimensioni massime dei file per un volume FAT16 sono di 2 GB.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                    | Non è possibile creare il disco rigido virtuale dopo l'avvio dell'arresto dell'applicazione.<br/>                                                             |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                    |



 

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

 

