---
title: Metodo IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces.h)
description: Crea un disco rigido virtuale differenze.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Metodo CreateDifferencingVirtualHardDisk Virtual PC
- Metodo CreateDifferencingVirtualHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateDifferencingVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b065d7b1d7a5f5f21aa0120b58d4ca2dc9177d0a48f6b2389365ee37811883c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394421"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a>Metodo IVMVirtualPC::CreateDifferencingVirtualHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Crea un disco rigido virtuale differenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*imagePath* \[ Pollici\]
</dt> <dd>

Percorso del nuovo file di immagine del disco. La cartella contenitore verrà creata se non esiste.

</dd> <dt>

*parentPath* \[ Pollici\]
</dt> <dd>

Percorso del file di immagine del disco padre.

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
| <dl> <dt>**HRESULT \_ DA \_ WIN32(PERCORSO \_ ERRORE NON \_ \_ TROVATO) 0X80070003**</dt> <dt></dt> </dl> | Il sistema non riesce a trovare il percorso specificato dal *parametro imagePath* *o parentPath.*<br/>                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0x8007000f</dt> </dl>   | Il file specificato dal *parametro imagePath* si trova in un CD-ROM o DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro imagePath* *o parentPath* contiene un carattere non valido (uno di " \* ?:<>/ \| "").<br/>                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Sia il *parametro imagePath* che *il parametro parentPath* specificano un percorso vuoto o relativo. Almeno uno dei parametri deve essere un percorso assoluto.<br/>                                                                                       |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dai parametri *imagePath* *o parentPath* è troppo lungo. La lunghezza del percorso deve essere inferiore a 260 caratteri.<br/>                                                                                              |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>  | Il file a cui fa riferimento *il parametro imagePath* esiste già.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>       | L'immagine del disco rigido virtuale a espansione dinamica richiede almeno 8 MB di spazio disponibile nel volume host.<br/>                                                                                                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ DIMENSIONI \_ \_ DELL'IMMAGINE TROPPO \_ GRANDI**</dt> <dt>0XA0040683</dt> </dl>                | Le dimensioni *del* parametro devono essere inferiori a 2.088.960 MB. Se il formato è FAT16, le dimensioni devono essere inferiori a 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ DIMENSIONI \_ \_ DELL'IMMAGINE TROPPO PICCOLE \_ 0XA0040684**</dt> <dt></dt> </dl>                | Le immagini del disco rigido virtuale formattate e FAT16 non formattate devono essere di almeno 3 MB. Le immagini del disco rigido virtuale in formato FAT32 devono essere di almeno 514 MB.<br/>                                                                                   |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE TROPPO GRANDE PER \_ \_ \_ \_ VOLUME**</dt> <dt>0XA0040679</dt> </dl>          | Il volume host non può supportare un file di queste dimensioni se l'immagine del disco rigido virtuale in espansione dinamica si espande fino al limite completo. Le dimensioni massime del file per un volume FAT32 sono di 4 GB. Le dimensioni massime del file per un volume FAT16 sono di 2 GB.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ ARRESTO \_ DELL'APP \_ 0XA0040209**</dt> <dt></dt> </dl>                    | Non è possibile creare il disco rigido virtuale dopo l'avvio dell'arresto dell'applicazione.<br/>                                                                                                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0XA0040951</dt> </dl>     | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Anche se *imagePath* o *parentPath* può essere un percorso relativo, almeno uno di questi deve essere un percorso assoluto. Se un parametro path è un percorso relativo, si presuppone che sia relativo all'altro parametro path.

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

 

