---
title: Struttura LSLicense
description: Contiene informazioni su una licenza di Servizi Desktop remoto specifica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della struttura LSLicense
- Servizi Desktop remoto puntatore alla struttura LPLSLicense
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476439"
---
# <a name="lslicense-structure"></a>Struttura LSLicense

Contiene informazioni su una licenza di Servizi Desktop remoto specifica.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Versione della licenza.

</dd> <dt>

**dwLicenseId**
</dt> <dd>

ID della licenza.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID del [**LSKeyPack**](lskeypack.md) che contiene la licenza.

</dd> <dt>

**szHWID**
</dt> <dd>

ID hardware del client di Connessione Desktop remoto (RDC) che ha emesso la licenza.

</dd> <dt>

**szMachineName**
</dt> <dd>

Nome del client di Connessione Desktop remoto (RDC) che ha emesso la licenza.

</dd> <dt>

**szUserName**
</dt> <dd>

Nome dell'utente che ha emesso la licenza.

</dd> <dt>

**dwCertSerialLicense**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**dwLicenseSerialNumber**
</dt> <dd>

Numero di serie della licenza.

</dd> <dt>

**ftIssueDate**
</dt> <dd>

Data di rilascio della licenza.

</dd> <dt>

**ftExpireDate**
</dt> <dd>

Data di scadenza della licenza.

</dd> <dt>

**ucLicenseStatus**
</dt> <dd>

Stato corrente della licenza.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

 





