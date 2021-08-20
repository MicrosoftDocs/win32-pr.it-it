---
title: Metodo IVMHardDisk MergeTo (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 19f54c3e7cfcd328adcea355e90ff60d92590fb694915a3e682a6240b656e655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123721"
---
# <a name="ivmharddiskmergeto-method"></a>Metodo IVMHardDisk::MergeTo

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre (fino al disco rigido virtuale padre radice incluso) in un nuovo file del disco rigido.

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

*newDiskImagePath* \[ Pollici\]
</dt> <dd>

Percorso della nuova immagine del disco di destinazione in cui verranno unite le immagini disco selezionate.

</dd> <dt>

*newDiskImageType* \[ Pollici\]
</dt> <dd>

Tipo di nuova immagine del disco di destinazione. I tipi di immagine consentiti per la nuova immagine del disco di destinazione sono **vmDiskType \_ Dynamic** e **vmDiskType \_ FixedSize**. Per altre informazioni, vedere [**VMHardDiskType.**](vmharddisktype.md)

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Oggetto [**IVMTask**](ivmtask.md) usato per tenere traccia del completamento del processo di unione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'operazione è stata completata.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                      | Un parametro è **NULL.**<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Il *parametro newDiskImagePath* è vuoto.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(FILE \_ DI ERRORE NON \_ \_ TROVATO)**</dt> <dt>0X80070002</dt> </dl>   | Il sistema non riesce a trovare il file specificato dal *parametro newDiskImagePath.*<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND) 0X80070003**</dt> <dt></dt> </dl>   | Il sistema non riesce a trovare il percorso specificato dal *parametro newDiskImagePath.*<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>      | Il *parametro newDiskImagePath* contiene un carattere non valido (uno dei seguenti: " \* ?<>/ \| ":").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | Il *parametro newDiskImagePath* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | Il percorso specificato dal *parametro newDiskImagePath* è troppo lungo. Il percorso deve contenere meno di 260 caratteri.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(VIOLAZIONE \_ DI CONDIVISIONE \_ ERRORI)**</dt> <dt>0X80070020</dt> </dl> | Il disco rigido virtuale a cui fa riferimento questo oggetto è in uso o l'elemento padre di questo disco rigido virtuale è in uso.<br/>                                                                                                                                                                                |
| <dl> <dt>**Macchina virtuale \_ E \_ TIPO DI IMMAGINE HD \_ \_ \_ 0XA004067B**</dt> <dt></dt> </dl>                   | Questo errore è causato dal fatto che l'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non è un'immagine disco differenze o perché il parametro *newDiskImageType* non è uno dei valori accettati, **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>    | Il file a cui fa riferimento *il parametro newDiskImagePath* esiste già.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | Il volume host non dispone di spazio sufficiente per unire questo disco rigido virtuale.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ PERCORSO PADRE NON TROVATO \_ \_ \_ 0XA0040677**</dt> <dt></dt> </dl>                 | L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto non esiste.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ ARRESTO \_ DELL'APP \_ 0XA0040209**</dt> <dt></dt> </dl>                      | Impossibile unire l'immagine del disco rigido virtuale perché l'applicazione è in fase di arresto.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk è definito come \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

