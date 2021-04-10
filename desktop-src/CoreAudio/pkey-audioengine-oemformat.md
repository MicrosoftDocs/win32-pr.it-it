---
description: La \_ Proprietà pkey Audioengine \_ OEMFormat specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione di un flusso. I valori vengono popolati dall'OEM in un file con estensione inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127427"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ Audioengine \_ OEMFormat

La \_ Proprietà pkey Audioengine \_ OEMFormat specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione di un flusso. I valori vengono popolati dall'OEM in un file con estensione inf.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ BLOB.

Il membro **BLOB** della struttura **PROPVARIANT** è una struttura di tipo **BLOB** che contiene due membri. Member **BLOB. cbSize** è un **valore DWORD** che specifica il numero di byte nella descrizione del formato. Il membro **BLOB. pBlobData** punta a una struttura **WAVEFORMATEX** che contiene la descrizione del formato. Per ulteriori informazioni su BLOB, vedere la documentazione Windows SDK. Per ulteriori informazioni su **WAVEFORMATEX**, vedere la documentazione di Windows DDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




