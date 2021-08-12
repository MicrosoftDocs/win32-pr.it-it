---
title: Struttura WMDMRIGHTS
description: La struttura WMDMRIGHTS descrive i diritti di utilizzo del contenuto.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Struttura WMDMRIGHTS di Windows Media Device Manager
- Puntatore alla struttura PWMDMRIGHTS windows Media Device Manager
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
ms.openlocfilehash: 6b54713add3bef1c51d18fea3f66ac4b3e2e8ff1a066bcd83781f0f522d5a4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583984"
---
# <a name="wmdmrights-structure"></a>Struttura WMDMRIGHTS

La **struttura WMDMRIGHTS** descrive i diritti di utilizzo del contenuto.

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

Dimensioni della struttura, in byte.

</dd> <dt>

**dwContentType**
</dt> <dd>

**Valore DWORD** contenente il tipo di contenuto.

</dd> <dt>

**fuFlags**
</dt> <dd>

Campo di bit che specifica le opzioni relative ai diritti in uso per il contenuto.



| Valore                        | Descrizione                                  |
|------------------------------|----------------------------------------------|
| WMDM \_ RIGHTS \_ PLAYBACKCOUNT  | Numero di volte in cui è possibile riprodurre il file. |
| DATA DI SCADENZA DIRITTI WMDM \_ \_ | Data di scadenza del file.                 |
| DIRITTI WMDM \_ \_ FREESERIALIDS  | Identificatore seriale libero del file.          |
| Gruppo \_ GROUPID DIRITTI WMDM \_  | Identificatore del file.                      |
| DIRITTI WMDM \_ \_ DENOMINATISERIALIDS | Identificatore seriale denominato del file.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Campo di bit contenente i bit dei diritti per il contenuto.



| Valore                                     | Descrizione                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ RIGHTS \_ PLAY \_ ON \_ PC                | Il contenuto può essere riprodotto in un personal computer. |
| COPIA DEI DIRITTI \_ WMDM IN UN DISPOSITIVO NON \_ \_ \_ \_ \_ SDMI | Il contenuto può essere copiato in un dispositivo non SDMI.   |
| DIRITTI DI WMDM \_ \_ COPIA SU \_ \_ CD                | Il contenuto può essere copiato in un CD.                |
| COPIA DEI DIRITTI WMDM \_ \_ NEL DISPOSITIVO \_ \_ \_ SDMI      | Il contenuto può essere copiato in un dispositivo SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Matrice di byte che specifica il livello minimo di sicurezza dell'applicazione.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**Valore DWORD** contenente il numero di volte rimanenti in cui è possibile eseguire il rendering del contenuto.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

[**Struttura WMDMDATETIME**](wmdmdatetime.md) contenente la data e l'ora di scadenza del contenuto. Se la licenza non ha una data di scadenza, il membro **wYear** viene impostato su 0xFFFF e tutti gli altri membri di **WMDMDATETIME** vengono ignorati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





