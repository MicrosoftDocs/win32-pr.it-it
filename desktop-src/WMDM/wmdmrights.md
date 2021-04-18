---
title: Struttura WMDMRIGHTS
description: La struttura WMDMRIGHTS descrive i diritti di utilizzo del contenuto.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Struttura WMDMRIGHTS Windows Media Gestione dispositivi
- Puntatore alla struttura PWMDMRIGHTS Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325004"
---
# <a name="wmdmrights-structure"></a>Struttura WMDMRIGHTS

La struttura **WMDMRIGHTS** descrive i diritti di utilizzo del contenuto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensioni, in byte, della struttura.

</dd> <dt>

**dwContentType**
</dt> <dd>

**DWORD** che contiene il tipo di contenuto.

</dd> <dt>

**fuFlags**
</dt> <dd>

Campo di bit che specifica le opzioni dei diritti in uso per il contenuto.



| Valore                        | Descrizione                                  |
|------------------------------|----------------------------------------------|
| \_diritti WMDM \_ PLAYBACKCOUNT  | Numero di volte in cui il file può essere riprodotto. |
| \_diritti WMDM \_ EXPIRATIONDATE | Data di scadenza del file.                 |
| \_diritti WMDM \_ FREESERIALIDS  | Identificatore seriale gratuito del file.          |
| \_Gruppo GROUPID Rights WMDM \_  | Identificatore del file.                      |
| \_diritti WMDM \_ NAMEDSERIALIDS | Identificatore seriale denominato del file.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Campo di bit contenente i bit dei diritti per il contenuto.



| Valore                                     | Descrizione                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ Rights \_ Play \_ sul \_ PC                | Il contenuto può essere riprodotto in un personal computer. |
| \_Copia diritti \_ WMDM \_ nel \_ \_ dispositivo non SDMI \_ | Il contenuto può essere copiato in un dispositivo non SDMI.   |
| \_Copia diritti \_ WMDM \_ su \_ CD                | Il contenuto può essere copiato in un CD.                |
| \_Copia diritti \_ WMDM \_ nel \_ \_ dispositivo SDMI      | Il contenuto può essere copiato in un dispositivo SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Matrice di byte che specifica il livello minimo di sicurezza dell'applicazione.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** contenente il numero di volte rimanenti di cui è possibile eseguire il rendering del contenuto.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

Struttura [**WMDMDATETIME**](wmdmdatetime.md) contenente la data e l'ora di scadenza per il contenuto. Se la licenza non ha una data di scadenza, il membro **wYear** è impostato su 0xffff e tutti gli altri membri di **WMDMDATETIME** vengono ignorati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPStorage:: getrights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage:: getrights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





