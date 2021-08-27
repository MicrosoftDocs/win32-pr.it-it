---
title: WINBIO_IDENTITY struttura (Winbio \_ types.h)
description: Contiene un valore di identificazione associato a un modello biometrico.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY struttura Windows'API Biometric Framework
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
ms.openlocfilehash: c677a341386bcc937061798f406397028c23c10b65989480da975a9fdf81a3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910119"
---
# <a name="winbio_identity-structure"></a>Struttura WINBIO \_ IDENTITY

La **struttura WINBIO \_ IDENTITY** contiene un valore di identificazione associato a un modello biometrico.

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

Specifica il formato delle informazioni sull'identità contenute in questa struttura. I valori possibili sono i seguenti:



| Valore                                                                                                                                                                                         | Significato                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**TIPO DI ID WINBIO \_ \_ \_ NULL**</dt> </dl>             | Al modello non è associato alcun ID.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**CARATTERE JOLLY DI TIPO ID WINBIO \_ \_ \_**</dt> </dl> | La struttura corrisponde a tutte le identità del modello.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**GUID DEL TIPO \_ DI \_ \_ ID WINBIO**</dt> </dl>             | La struttura contiene un GUID associato al modello.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**SID DEL TIPO DI ID WINBIO \_ \_ \_**</dt> </dl>                | La struttura contiene il SID dell'account associato al modello.<br/> |



 

</dd> <dt>

**Valore**
</dt> <dd>

Unione che può contenere uno dei valori seguenti:

<dl> <dt>

**Null**
</dt> <dd>

Contiene 1 se il **membro Type** è **WINBIO \_ ID TYPE \_ \_ NULL.**

</dd> <dt>

**Carattere jolly**
</dt> <dd>

Contiene 1 se il **membro Type** è **WINBIO \_ ID TYPE \_ \_ WILDCARD**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contiene un valore GUID a 128 bit che identifica il modello se il membro **Type** è **WINBIO \_ ID TYPE \_ \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Struttura che contiene un SID dell'account se il membro **Type** è **WINBIO \_ ID TYPE \_ \_ SID**.

<dl> <dt>

**Dimensioni**
</dt> <dd>

Numero di caratteri nel SID.

</dd> <dt>

**Dati**
</dt> <dd>

Matrice di caratteri senza segno che contengono il SID. La dimensione massima corrente della matrice è di 68 caratteri.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata nelle funzioni seguenti:

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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> </dl>

 

 





