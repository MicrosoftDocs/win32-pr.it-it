---
description: Contiene l'intestazione dell'elenco di revoche globale (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Struttura GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305368"
---
# <a name="grl_header-structure"></a>\_Struttura dell'intestazione GRL

Contiene l'intestazione dell'elenco di revoche globale (GRL).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**wszIdentifier**
</dt> <dd>

Identificatore GRL. Il valore è sempre L "MSGRL".

</dd> <dt>

**wFormatMajor**
</dt> <dd>

Numero di versione principale. Attualmente, il valore deve essere 1.

</dd> <dt>

**wFormatMinor**
</dt> <dd>

Numero di versione secondario. Attualmente, il valore deve essere zero.

</dd> <dt>

**CreationTime**
</dt> <dd>

Valore **FILETIME** che specifica quando è stato creato il file.

</dd> <dt>

**dwSequenceNumber**
</dt> <dd>

Numero di versione di GRL. Attualmente, il valore deve essere almeno 3

</dd> <dt>

**dwForceRebootVersion**
</dt> <dd>

Riservato.

</dd> <dt>

**dwForceProcessRestartVersion**
</dt> <dd>

Riservato.

</dd> <dt>

**cbRevocationSectionOffset**
</dt> <dd>

Offset, in byte, dall'inizio del GRL alla sezione di base.

</dd> <dt>

**cRevokedKernelBinaries**
</dt> <dd>

Numero di file binari del kernel revocati elencati in GRL.

</dd> <dt>

**cRevokedUserBinaries**
</dt> <dd>

Numero di file binari revocati in modalità utente elencati in GRL.

</dd> <dt>

**cRevokedCertificates**
</dt> <dd>

Numero di certificati revocati elencati in GRL.

</dd> <dt>

**cTrustedRoots**
</dt> <dd>

Il numero di radici attendibili elencate in GRL.

</dd> <dt>

**cbExtensibleSectionOffset**
</dt> <dd>

Offset, in byte, dall'inizio di GRL alla sezione estendibile.

</dd> <dt>

**cExtensibleEntries**
</dt> <dd>

Numero di voci nella sezione estendibile.

</dd> <dt>

**cbRenewalSectionOffset**
</dt> <dd>

Offset, in byte, dall'inizio del GRL alla sezione rinnovi.

</dd> <dt>

**cRevokedKernelBinaryRenewals**
</dt> <dd>

Il numero di rinnovi binari del kernel elencati in GRL.

</dd> <dt>

**cRevokedUserBinaryRenewals**
</dt> <dd>

Il numero di rinnovi binari in modalità utente elencati in GRL.

</dd> <dt>

**cRevokedCertificateRenewals**
</dt> <dd>

Il numero di rinnovi certificati elencati in GRL.

</dd> <dt>

**cbSignatureCoreOffset**
</dt> <dd>

Offset, in byte, dall'inizio di GRL alla firma della sezione di base.

</dd> <dt>

**cbSignatureExtOffset**
</dt> <dd>

Offset, in byte, dall'inizio del GRL alla firma della sezione estendibile.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i numeri interi in GRL hanno un ordine di byte little-endian. Tutte le strutture sono allineate ai limiti di 1 byte.

Questa struttura non è dichiarata in un'intestazione SDK. Per usare questa struttura, aggiungere la dichiarazione mostrata qui al codice sorgente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Revoca del certificato OPM](opm-certificate-revocation.md)
</dt> <dt>

[Strutture OPM](opm-structures.md)
</dt> </dl>

 

 




