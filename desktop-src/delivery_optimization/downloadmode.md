---
title: Enumerazione DownloadMode (Deliveryoptimization.h)
description: Definisce le diverse modalità di download utilizzate Ottimizzazione recapito download.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- In questa modalità Ottimizzazione recapito viene ignorato e al suo posto viene usato BITS. Seleziona ad esempio questa modalità per consentire ai client di usare BranchCache. enumerazione
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ea753ef47dc2e6655d7e707466d7b0448bee7bec1f090b1baf4de04799283d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543725"
---
# <a name="downloadmode-enumeration"></a>Enumerazione DownloadMode

Definisce le diverse modalità di download utilizzate Ottimizzazione recapito download.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

Questa impostazione disabilita la memorizzazione nella cache peer-to-peer, ma Ottimizzazione recapito di scaricare contenuto dai server Microsoft. Questa modalità usa metadati aggiuntivi forniti dall'Ottimizzazione recapito cloud per un'esperienza di download affidabile ed efficiente senza peer.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Questa modalità operativa predefinita per Ottimizzazione recapito consente la condivisione peer sulla stessa rete.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

Quando è impostata la modalità gruppo, il gruppo viene selezionato automaticamente in base al sito Active Directory Domain Services (AD DS) del dispositivo (Windows 10, versione 1607) o al dominio in cui viene autenticato il dispositivo (Windows 10, versione 1511). In modalità di gruppo, il peering avviene tra le subnet interne, tra i dispositivi che appartengono allo stesso gruppo, inclusi i dispositivi nelle sedi remote. Puoi usare l'opzione GroupID per creare un gruppo personalizzato indipendentemente dai domini e dai siti di Servizi di dominio Active Directory. La modalità di download di gruppo è l'opzione consigliata per la maggior parte delle organizzazioni che vuole ottenere la massima ottimizzazione della larghezza di banda con Ottimizzazione recapito.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Questa modalità abilita le origini peer Internet per Ottimizzazione recapito.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

La modalità semplice disabilita completamente l'uso dei servizi cloud di Ottimizzazione recapito (per gli ambienti offline). Ottimizzazione recapito questa modalità passa automaticamente quando i servizi cloud Ottimizzazione recapito non sono disponibili, non raggiungibili o quando le dimensioni del file di contenuto sono inferiori a 10 MB. In questa modalità, Ottimizzazione recapito un'esperienza di download affidabile, senza memorizzazione nella cache peer-to-peer.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

In questa modalità Ottimizzazione recapito viene ignorato e al suo posto viene usato BITS. Seleziona ad esempio questa modalità per consentire ai client di usare BranchCache.

</dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------|----------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>      |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>  |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>               |
