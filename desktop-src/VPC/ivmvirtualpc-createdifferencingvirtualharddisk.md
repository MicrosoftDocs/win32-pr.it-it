---
title: Metodo IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces. h)
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
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302337"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a>Metodo IVMVirtualPC:: CreateDifferencingVirtualHardDisk

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*imagePath* \[ in\]
</dt> <dd>

Percorso del nuovo file di immagine del disco. Se non esiste, verrà creata la cartella che lo contiene.

</dd> <dt>

*ParentPath* \[ in\]
</dt> <dd>

Percorso del file di immagine del disco padre.

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia della creazione dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Un parametro è **null**.<br/>                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl> | Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* o *ParentPath* .<br/>                                                                                                                                             |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ unità non valida \_ )**</dt> <dt>0x8007000f</dt> </dl>   | Il file specificato dal parametro *imagePath* si trova su un CD-ROM o un DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>    | Il parametro *imagePath* o *ParentPath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").<br/>                                                                                                                                |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *imagePath* e *ParentPath* specifica un percorso vuoto o relativo. Almeno uno dei parametri deve essere un percorso assoluto.<br/>                                                                                       |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dai parametri *imagePath* o *ParentPath* è troppo lungo. La lunghezza del percorso deve essere inferiore a 260 caratteri.<br/>                                                                                              |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt> </dl>  | Il file a cui fa riferimento il parametro *imagePath* esiste già.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt> </dl>       | Per l'immagine del disco rigido virtuale a espansione dinamica sono necessari almeno 8 MB di spazio sul volume host.<br/>                                                                                                                                      |
| <dl> <dt>**Macchina virtuale \_ Dimensioni dell'immagine E 0xA0040683 \_ \_ \_ troppo \_ grandi**</dt> <dt></dt> </dl>                | Le *dimensioni* del parametro devono essere minori di 2.088.960 MB. Se il formato è FAT16, le dimensioni devono essere minori di 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**Macchina virtuale \_ \_Dimensioni immagine E \_ dimensioni \_ troppo \_ ridotte**</dt> <dt>0xA0040684</dt> </dl>                | Le immagini del disco rigido virtuale in formato FAT16 e non formattato devono essere di almeno 3 MB. Le immagini del disco rigido virtuale formattato FAT32 devono essere di almeno 514 MB.<br/>                                                                                   |
| <dl> <dt>**Macchina virtuale \_ Il \_ file E è \_ troppo \_ grande \_ per il \_ volume**</dt> <dt>0xA0040679</dt> </dl>          | Il volume host non può supportare un file di questa dimensione se l'immagine del disco rigido virtuale a espansione dinamica si espande fino al limite massimo. Le dimensioni massime del file per un volume FAT32 sono pari a 4 GB. Le dimensioni massime del file per un volume FAT16 sono pari a 2 GB.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt> </dl>                    | Non è possibile creare il disco rigido virtuale dopo che l'applicazione è stata avviata.<br/>                                                                                                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl>     | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/>                                                                                                                                                |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Anche se *imagePath* o *ParentPath* può essere un percorso relativo, almeno uno di questi deve essere un percorso assoluto. Se un parametro path è un percorso relativo, si presuppone che sia relativo all'altro parametro path.

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

 

