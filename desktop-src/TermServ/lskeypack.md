---
title: Struttura LSKeyPack
description: Contiene informazioni su un key pack specifico Servizi Desktop remoto licenze.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Struttura LSKeyPack Servizi Desktop remoto
- Puntatore alla struttura LPLSKeyPack Servizi Desktop remoto
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8b2c7c8b6c42464e273008f9de2730b41ea64981e44583eb48f4125da3ba9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989090"
---
# <a name="lskeypack-structure"></a>Struttura LSKeyPack

Contiene informazioni su un key pack specifico Servizi Desktop remoto licenze.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Versione del key pack.

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

Tipo di key pack.

</dd> <dt>

**szCompanyName**
</dt> <dd>

Nome della società che ha emesso il key pack.

</dd> <dt>

**szKeyPackId**
</dt> <dd>

ID del key pack.

</dd> <dt>

**szProductName**
</dt> <dd>

Nome del prodotto a cui appartiene questo Key Pack.

</dd> <dt>

**szProductId**
</dt> <dd>

ID del prodotto a cui appartiene questo key pack.

</dd> <dt>

**szProductDesc**
</dt> <dd>

Descrizione del prodotto a cui appartiene questo Key Pack.

</dd> <dt>

**wMajorVersion**
</dt> <dd>

Versione principale del prodotto a cui appartiene questo Key Pack.

</dd> <dt>

**wMinorVersion**
</dt> <dd>

Versione secondaria del prodotto a cui appartiene questo Key Pack.

</dd> <dt>

**dwPlatformType**
</dt> <dd>

Tipo di piattaforma.

</dd> <dt>

**ucLicenseType**
</dt> <dd>

Tipo di licenze nel Key Pack.

</dd> <dt>

**dwLanguageId**
</dt> <dd>

ID della lingua.

</dd> <dt>

**ucChannelOfPurchase**
</dt> <dd>

Canale di acquisto.

</dd> <dt>

**szBeginSerialNumber**
</dt> <dd>

Numero di serie per la prima licenza.

</dd> <dt>

**dwTotalLicenseInKeyPack**
</dt> <dd>

Numero totale di licenze nel key pack.

</dd> <dt>

**dwProductFlags**
</dt> <dd>

Bandiere.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID del key pack.

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

Stato del key pack.

</dd> <dt>

**dwActivateDate**
</dt> <dd>

Data di attivazione per il key pack.

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

Data di scadenza del key pack.

</dd> <dt>

**dwNumberOfLicenses**
</dt> <dd>

Numero di licenze.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

 





