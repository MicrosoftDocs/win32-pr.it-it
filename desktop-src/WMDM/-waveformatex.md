---
title: _WAVEFORMATEX struttura
description: La struttura \_WAVEFORMATEX definisce il formato dei dati audio della forma d’onda
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX struttura windows Media Device Manager
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e149608d740df6df40b39b64b09ac11837a721b5b4844f1a73eb52e1b5cea479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586746"
---
# <a name="_waveformatex-structure"></a>\_Struttura WAVEFORMATEX

La **\_ struttura WAVEFORMATEX** definisce il formato dei dati waveform-audio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>Members

<dl> <dt>

**wFormatTag**
</dt> <dd>

Deve essere impostato su uno o più formati supportati dal dispositivo. Si noti che nelle versioni precedenti di Windows Media Device Manager è consigliabile usare WMDM WAVE FORMAT ALL per \_ indicare il supporto per tutti i \_ \_ formati. Tuttavia, questa operazione non è più consigliata, perché lettori multimediali diversi interpretano questa operazione in modi diversi e pochi dispositivi possono effettivamente riprodurre qualsiasi formato di file. È ora consigliabile usare il valore WMDM ENUM PROP VALID VALUES ANY dell'enumerazione \_ \_ \_ \_ \_ [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM**](wmdm-enum-prop-valid-values-form.md) [**\_ \_ \_**](wmdm-prop-values-range.md) oppure specificare meglio un intervallo di formati con la struttura WMDM PROP VALUES RANGE.

</dd> <dt>

**nChannels**
</dt> <dd>

Numero di canali nei dati waveform-audio. I dati monaurali utilizzano un canale e i dati stereo utilizzano due canali.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Frequenza di campionamento, in campioni al secondo (Hertz), in cui ogni canale deve essere riprodotto o registrato. I valori comuni per **nSamplesPerSec** sono 8,0 kilohertz (kHz), 11,025 kHz, 22,05 kHz e 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Velocità media di trasferimento dei dati necessaria per il tag di formato, in byte al secondo. Il software di riproduzione e registrazione può stimare le dimensioni del buffer usando il membro **nAvgBytesPerSec.**

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Allineamento del blocco, in byte. L'allineamento dei blocchi è l'unità atomica minima di dati per il tipo di formato **wFormatTag.** Il software di riproduzione e registrazione deve elaborare un multiplo di byte di dati **nBlockAlign** alla volta. I dati scritti e letti da un dispositivo devono sempre iniziare all'inizio di un blocco. Ad esempio, non è possibile avviare correttamente la riproduzione di dati PCM nel mezzo di un campione, ovvero su un limite non allineato a blocchi.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bit per esempio per il **tipo di formato wFormatTag.**

</dd> <dt>

**cbSize**
</dt> <dd>

Questo membro viene ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





