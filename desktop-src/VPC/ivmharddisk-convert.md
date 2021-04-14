---
title: Metodo Convert IVMHardDisk (VPCCOMInterfaces. h)
description: Converte un disco rigido virtuale a dimensione fissa in un disco rigido virtuale a espansione dinamica o converte un disco rigido virtuale a espansione dinamica in un disco rigido virtuale a dimensione fissa.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convertire il metodo Virtual PC
- Convert Method Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, Convert (metodo)
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
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478803"
---
# <a name="ivmharddiskconvert-method"></a>Metodo IVMHardDisk:: Convert

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Converte un disco rigido virtuale a dimensione fissa in un disco rigido virtuale a espansione dinamica o converte un disco rigido virtuale a espansione dinamica in un disco rigido virtuale a dimensione fissa.

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

*convertedDiskImagePath* \[ in\]
</dt> <dd>

Percorso del file di immagine del disco di destinazione.

</dd> <dt>

*convertedDiskImageType* \[ in\]
</dt> <dd>

Tipo di immagine del disco di destinazione. Per un elenco di valori, vedere [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di conversione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                        |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                   | Il parametro *convertedDiskImagePath* è vuoto o manca l'estensione VHD sul nome del file.<br/>                                      |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                      | Un parametro è **null**.<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl>   | Il sistema non è in grado di trovare il percorso specificato dal parametro *convertedDiskImagePath* .<br/>                                                 |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>      | Il parametro *convertedDiskImagePath* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>      | Il parametro *convertedDiskImagePath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                            |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | Il percorso specificato dal parametro *convertedDiskImagePath* è troppo lungo. Il percorso deve essere minore di **Max \_ path** (260) caratteri.<br/> |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt> </dl> | Il disco rigido virtuale a cui fa riferimento questo oggetto è in uso o l'elemento padre di questo disco rigido virtuale è in uso.<br/>                  |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt> </dl>         | Il volume host non dispone di spazio sufficiente per la conversione del disco rigido virtuale.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt> </dl>    | Il file a cui fa riferimento il parametro *convertedDiskImagePath* esiste già.<br/>                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt> </dl>                   | Il parametro *convertedDiskImagePath* deve essere **VmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.<br/>                          |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ \_ file HD non valido**</dt> <dt>0xA0040682</dt> </dl>                        | L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non sembra essere un'immagine valida.<br/>          |
| <dl> <dt>**Macchina virtuale \_ \_Percorso padre \_ E \_ non \_ trovato**</dt> <dt>0xA0040677</dt> </dl>                 | L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto non esiste.<br/>                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt> </dl>                      | Non è possibile convertire l'immagine del disco rigido virtuale perché è in corso la chiusura dell'applicazione.<br/>                                            |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il file di origine viene lasciato intatto dopo il processo di conversione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

