---
title: Metodo Convert IVMHardDisk (VPCCOMInterfaces.h)
description: Converte un disco rigido virtuale di dimensioni fisse in un disco rigido virtuale a espansione dinamica o un disco rigido virtuale a espansione dinamica in un disco rigido virtuale di dimensioni fisse.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Metodo Convert Virtual PC
- Metodo Convert Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e509c683ef86e169eb07d661c9682d8ed67204bcc7e1651d2d6370ee4be82f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593884"
---
# <a name="ivmharddiskconvert-method"></a>Metodo IVMHardDisk::Convert

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Converte un disco rigido virtuale di dimensioni fisse in un disco rigido virtuale a espansione dinamica o un disco rigido virtuale a espansione dinamica in un disco rigido virtuale di dimensioni fisse.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*convertedDiskImagePath* \[ Pollici\]
</dt> <dd>

Percorso del file di immagine del disco di destinazione.

</dd> <dt>

*convertedDiskImageType* \[ Pollici\]
</dt> <dd>

Tipo dell'immagine del disco di destinazione. Per un elenco di valori, vedere [**VMHardDiskType.**](vmharddisktype.md)

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia del completamento del processo di conversione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Il *parametro convertedDiskImagePath* è vuoto o manca l'estensione vhd nel nome file.<br/>                                      |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                      | Un parametro è **NULL.**<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl>   | Il sistema non riesce a trovare il percorso specificato dal *parametro convertedDiskImagePath.*<br/>                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>      | Il *parametro convertedDiskImagePath* contiene un carattere non valido (uno tra " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | Il *parametro convertedDiskImagePath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | Il percorso specificato dal *parametro convertedDiskImagePath* è troppo lungo. Il percorso deve essere minore di **MAX \_ PATH** (260).<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0x80070020</dt> </dl> | Il disco rigido virtuale a cui fa riferimento questo oggetto è in uso o l'elemento padre di questo disco rigido virtuale è in uso.<br/>                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | Il volume host non dispone di spazio sufficiente per convertire il disco rigido virtuale.<br/>                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>    | Il file a cui fa riferimento *il parametro convertedDiskImagePath* esiste già.<br/>                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ TIPO DI IMMAGINE HD \_ \_ \_ ERRATO**</dt> <dt>0XA004067B</dt> </dl>                   | Il *parametro convertedDiskImagePath* deve essere **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize.**<br/>                          |
| <dl> <dt>**Macchina virtuale \_ E \_ FILE HD NON \_ \_ VALIDO**</dt> <dt>0xA0040682</dt> </dl>                        | L'immagine del disco rigido virtuale a cui fa riferimento questo [**oggetto IVMHardDisk**](ivmharddisk.md) non sembra essere un'immagine valida.<br/>          |
| <dl> <dt>**Macchina virtuale \_ E \_ PERCORSO PADRE NON TROVATO \_ \_ \_ 0XA0040677**</dt> <dt></dt> </dl>                 | L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto non esiste.<br/>                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ APP \_ SHUTTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | L'immagine del disco rigido virtuale non può essere convertita perché l'applicazione è in fase di arresto.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il file di origine viene lasciato intatto dopo il processo di conversione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

