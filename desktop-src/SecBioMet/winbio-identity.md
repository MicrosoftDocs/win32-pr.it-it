---
title: Struttura WINBIO_IDENTITY ( \_ tipi WINBIO. h)
description: Contiene un valore di identificazione associato a un modello biometrico.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- Struttura di WINBIO_IDENTITY Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119982"
---
# <a name="winbio_identity-structure"></a>\_Struttura di identità WINBIO

La struttura di **\_ identità WINBIO** contiene un valore di identificazione associato a un modello biometrico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Specifica il formato delle informazioni di identità contenute nella struttura. I valori possibili sono i seguenti:



| Valore                                                                                                                                                                                         | Significato                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_tipo di ID WINBIO \_ \_ null**</dt> </dl>             | Al modello non è associato alcun ID.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ carattere jolly tipo ID WINBIO \_**</dt> </dl> | La struttura corrisponde a tutte le identità del modello.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_ \_ GUID tipo ID \_ WINBIO**</dt> </dl>             | La struttura contiene un GUID associato al modello.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**\_ \_ SID tipo ID \_ WINBIO**</dt> </dl>                | La struttura contiene il SID dell'account associato al modello.<br/> |



 

</dd> <dt>

**Valore**
</dt> <dd>

Unione che può contenere uno dei valori seguenti:

<dl> <dt>

**Null**
</dt> <dd>

Contiene 1 se il membro del **tipo** è **WINBIO \_ ID \_ tipo \_ null**.

</dd> <dt>

**Jolly**
</dt> <dd>

Contiene 1 se il membro del **tipo** è un **\_ \_ \_ carattere jolly di tipo ID WINBIO**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contiene un valore GUID a 128 bit che identifica il modello se il membro del **tipo** è **WINBIO \_ ID \_ tipo \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Struttura che contiene un SID dell'account se il membro di **tipo** è **WINBIO \_ ID \_ tipo \_ SID**.

<dl> <dt>

**Dimensioni**
</dt> <dd>

Numero di caratteri nel SID.

</dd> <dt>

**Dati**
</dt> <dd>

Matrice di caratteri non firmati che contengono il SID. La dimensione massima corrente della matrice è 68 caratteri.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata nelle funzioni seguenti:

-   [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> </dl>

 

 





