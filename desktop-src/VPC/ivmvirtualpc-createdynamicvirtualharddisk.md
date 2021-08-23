---
title: Metodo IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces.h)
description: Crea un disco rigido virtuale con ridimensionamento dinamico.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- Metodo CreateDynamicVirtualHardDisk virtual PC
- Metodo CreateDynamicVirtualHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6de505f2e8b47bc36b7537a3abcdab1f07e7551a8c5ed9caee9aed100288df51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998651"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a>Metodo IVMVirtualPC::CreateDynamicVirtualHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Crea un disco rigido virtuale con ridimensionamento dinamico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDynamicVirtualHardDisk(
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

Dimensioni dell'immagine, in megabyte. Questo valore può essere al massimo 2.088.960 MB (2040 GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia della creazione dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Un parametro è **NULL.**<br/>                                                                                                                                                                                                            |
| <dl> <dt>**E \_ InvalidARG**</dt> <dt>0x80000003</dt> </dl>                                 | Il *parametro size* è minore o uguale a 0.<br/>                                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro imagePath.*<br/>                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0x8007000f</dt> </dl>   | Il file specificato dal *parametro imagePath* si trova in un CD-ROM o DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro imagePath* contiene un carattere non valido (uno tra " \* ?:<>/ \| "").<br/>                                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Entrambi i *parametri imagePath* specificano un percorso vuoto o relativo. Almeno uno dei parametri deve essere un percorso assoluto.<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro imagePath* è troppo lungo. La lunghezza del percorso deve essere minore di 260 caratteri.<br/>                                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | Il file a cui fa riferimento *il parametro imagePath* esiste già.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | L'immagine del disco rigido virtuale a espansione dinamica richiede almeno 8 MB di spazio disponibile nel volume host.<br/>                                                                                                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ DIMENSIONI \_ \_ DELL'IMMAGINE TROPPO \_ GRANDI**</dt> <dt>0XA0040683</dt> </dl>                | Le dimensioni *del* parametro devono essere inferiori a 2.088.960 MB. Se il formato è FAT16, le dimensioni devono essere inferiori a 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ DIMENSIONI \_ \_ DELL'IMMAGINE TROPPO PICCOLE \_ 0XA0040684**</dt> <dt></dt> </dl>                | Le immagini di dischi rigidi virtuali formattati non formattati e FAT16 devono essere di almeno 3 MB. Le immagini del disco rigido virtuale in formato FAT32 devono essere di almeno 514 MB.<br/>                                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE TOO LARGE FOR \_ \_ \_ \_ VOLUME**</dt> <dt>0xA0040679</dt> </dl>          | Il volume host non può supportare un file di queste dimensioni se l'immagine del disco rigido virtuale a espansione dinamica si espande fino al limite completo. Le dimensioni massime dei file per un volume FAT32 sono di 4 GB. Le dimensioni massime dei file per un volume FAT16 sono di 2 GB.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                    | Non è possibile creare il disco rigido virtuale dopo l'avvio dell'arresto dell'applicazione.<br/>                                                                                                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                   |



 

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

 

