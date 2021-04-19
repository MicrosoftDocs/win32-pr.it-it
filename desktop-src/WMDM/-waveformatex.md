---
title: Struttura _WAVEFORMATEX
description: La struttura \_WAVEFORMATEX definisce il formato dei dati audio della forma d’onda
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Struttura di _WAVEFORMATEX Windows Media Gestione dispositivi
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
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326482"
---
# <a name="_waveformatex-structure"></a>\_Struttura WAVEFORMATEX

La struttura **\_ WAVEFORMATEX** definisce il formato dei dati audio della forma d'onda.

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

Deve essere impostato su un formato o su formati supportati dal dispositivo. Si noti che le versioni precedenti di Windows Media Gestione dispositivi consigliate con WMDM \_ Wave \_ Format \_ all per indicare il supporto per tutti i formati. Tuttavia, questa operazione non è più consigliata, in quanto i diversi lettori multimediali interpreteranno questa operazione in modi diversi e alcuni dispositivi potranno effettivamente riprodurre qualsiasi formato di file. È ora consigliabile usare WMDM \_ enum prop Valid values \_ \_ \_ \_ qualsiasi valore dell'enumerazione [**WMDM \_ enum \_ prop \_ valid \_ Values \_ form**](wmdm-enum-prop-valid-values-form.md) , oppure è opportuno specificare un intervallo di formati con la struttura [**WMDM \_ prop \_ Values \_ Range**](wmdm-prop-values-range.md) .

</dd> <dt>

**nChannels**
</dt> <dd>

Numero di canali nei dati audio della forma d'onda. I dati mono utilizzano un solo canale e i dati stereo utilizzano due canali.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Frequenza di campionamento, in campioni al secondo (hertz), in cui ogni canale deve essere riprodotto o registrato. I valori comuni per **nSamplesPerSec** sono 8,0 kilohertz (kHz), 11,025 khz, 22,05 khz e 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Velocità di trasferimento dati media necessaria per il tag di formato, in byte al secondo. Per la riproduzione e la registrazione del software è possibile stimare le dimensioni del buffer usando il membro **nAvgBytesPerSec** .

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Allineamento del blocco in byte. L'allineamento del blocco è l'unità atomica minima dei dati per il tipo di formato **wFormatTag** . La riproduzione e la registrazione del software devono elaborare un multiplo di byte di **nBlockAlign** di dati alla volta. I dati scritti e letti da un dispositivo devono sempre iniziare all'inizio di un blocco. Non è ad esempio possibile avviare correttamente la riproduzione dei dati PCM al centro di un campione (ovvero su un limite non allineato a blocchi).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bit per campione per il tipo di formato **wFormatTag** .

</dd> <dt>

**cbSize**
</dt> <dd>

Questo membro viene ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage:: CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





