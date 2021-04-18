---
title: Struttura OPAQUECOMMAND
description: La struttura OPAQUECOMMAND contiene i dati per i comandi passati attraverso Windows Media Gestione dispositivi a un dispositivo ma che non devono essere utilizzati da Windows Media Gestione dispositivi.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Struttura OPAQUECOMMAND Windows Media Gestione dispositivi
- struttura di Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328415"
---
# <a name="opaquecommand-structure"></a>Struttura OPAQUECOMMAND

La struttura **OPAQUECOMMAND** contiene i dati per i comandi passati attraverso windows media gestione dispositivi a un dispositivo ma che non devono essere utilizzati da windows media gestione dispositivi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**guidCommand**
</dt> <dd>

**GUID** che rappresenta il comando richiesto.

</dd> <dt>

**dwDataLen**
</dt> <dd>

Lunghezza dei dati a cui punta *pData* , in byte.

</dd> <dt>

**pData**
</dt> <dd>

Dati necessari per eseguire il comando e/o i dati restituiti dal comando.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Questo codice MAC (Message Authentication Code) deve includere il membro **guidCommand** , i dati a cui punta *pdwDataLen* e i dati a cui si riferiscono i punti di *pData* . Se *pData* è **null**, non deve essere incluso nel Mac. WMDM \_ Mac \_ length è definito come 20.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**IMDSPStorage::SendOpaqueCommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**IWMDMDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





