---
title: Metodo IVMHardDisk MergeTo (VPCCOMInterfaces. h)
description: Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Metodo MergeTo Virtual PC
- Metodo MergeTo Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo MergeTo
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119962"
---
# <a name="ivmharddiskmergeto-method"></a>Metodo IVMHardDisk:: MergeTo

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre (fino al disco rigido virtuale padre radice) in un nuovo file di disco rigido.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newDiskImagePath* \[ in\]
</dt> <dd>

Percorso della nuova immagine del disco di destinazione in cui verranno unite le immagini del disco selezionate.

</dd> <dt>

*newDiskImageType* \[ in\]
</dt> <dd>

Tipo di nuova immagine del disco di destinazione. I tipi di immagine consentiti per la nuova immagine del disco di destinazione sono **vmDiskType \_ Dynamic** e **vmDiskType \_ FixedSize**. Per ulteriori informazioni, vedere [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di Unione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                      | Un parametro è **null**.<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                   | Il parametro *newDiskImagePath* è vuoto.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt> </dl>   | Il sistema non è in grado di trovare il file specificato dal parametro *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt> </dl>   | Il sistema non è in grado di trovare il percorso specificato dal parametro *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>      | Il parametro *newDiskImagePath* contiene un carattere non valido (uno dei seguenti: " \* ? <>/ \| ": ").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>      | Il parametro *newDiskImagePath* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | Il percorso specificato dal parametro *newDiskImagePath* è troppo lungo. Il percorso deve essere composto da meno di 260 caratteri.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt> </dl> | Il disco rigido virtuale a cui fa riferimento questo oggetto è in uso o l'elemento padre di questo disco rigido virtuale è in uso.<br/>                                                                                                                                                                                |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt> </dl>                   | Questo errore è causato dal fatto che l'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non è un'immagine del disco differenze o perché il parametro *newDiskImageType* non è uno dei valori accettati, **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.<br/> |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt> </dl>    | Il file a cui fa riferimento il parametro *newDiskImagePath* esiste già.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt> </dl>         | Il volume host non dispone di spazio sufficiente per unire questo disco rigido virtuale.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**Macchina virtuale \_ \_Percorso padre \_ E \_ non \_ trovato**</dt> <dt>0xA0040677</dt> </dl>                 | L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto non esiste.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt> </dl>                      | Non è possibile eseguire il merge dell'immagine del disco rigido virtuale perché è in corso la chiusura dell'applicazione.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                                                                                  |



 

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

 

