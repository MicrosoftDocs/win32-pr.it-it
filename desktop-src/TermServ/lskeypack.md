---
title: Struttura LSKeyPack
description: Contiene informazioni su un Key Pack di gestione licenze Servizi Desktop remoto specifico.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della struttura LSKeyPack
- Servizi Desktop remoto puntatore alla struttura LPLSKeyPack
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964811"
---
# <a name="lskeypack-structure"></a>Struttura LSKeyPack

Contiene informazioni su un Key Pack di gestione licenze Servizi Desktop remoto specifico.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

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

Versione del Key Pack.

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

Tipo di Key Pack.

</dd> <dt>

**szCompanyName**
</dt> <dd>

Nome della società che ha emesso il Key Pack.

</dd> <dt>

**szKeyPackId**
</dt> <dd>

ID del Key Pack.

</dd> <dt>

**szProductName**
</dt> <dd>

Nome del prodotto a cui appartiene questo Key Pack.

</dd> <dt>

**szProductId**
</dt> <dd>

ID del prodotto a cui appartiene questo Key Pack.

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

Numero totale di licenze nel Key Pack.

</dd> <dt>

**dwProductFlags**
</dt> <dd>

Bandiere.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID del Key Pack.

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

Stato del Key Pack.

</dd> <dt>

**dwActivateDate**
</dt> <dd>

Data di attivazione per il Key Pack.

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

Data di scadenza per il Key Pack.

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

 

 





