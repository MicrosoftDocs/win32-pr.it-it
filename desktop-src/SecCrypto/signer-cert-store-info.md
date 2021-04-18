---
description: Specifica l'archivio certificati utilizzato per firmare un documento.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Struttura SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308109"
---
# <a name="signer_cert_store_info-structure"></a>Struttura delle \_ \_ informazioni dell'archivio certificati del firmatario \_

La struttura delle **\_ \_ \_ informazioni dell'archivio certificati del firmatario** specifica l'archivio certificati utilizzato per firmare un documento.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**pSigningCert**
</dt> <dd>

Puntatore a una struttura [**del \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato per il certificato di firma.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Specifica la modalità di aggiunta dei certificati alla firma. Per trovare la catena di certificati, vengono controllati gli archivi MY, CA, ROOT e SPC, oltre all'archivio specificato dal membro **hCertStore** . Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**\_ Firmatario \_ \_ Catena di criteri CERT**</dt> <dt>2 (0x2)</dt> </dl>                           | Aggiungere solo i certificati nella catena di certificati.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**\_ Firmatario \_Catena di criteri CERT \_ \_ senza \_ radice**</dt> <dt>8 (0x8)</dt> </dl> | Aggiungere solo i certificati nella catena di certificati, escluso il certificato radice.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**\_ Firmatario \_ \_ Archivio criteri CERT**</dt> <dt>1 (0x1)</dt> </dl>                           | Aggiungere tutti i certificati nell'archivio specificato dal membro **hCertStore** . Questo flag può essere **una combinazione OR bit per** bit con uno degli altri valori possibili per questo membro.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

facoltativo. Handle per un archivio certificati aggiuntivo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**certificato FIRMATARIo \_**](signer-cert.md)
</dt> </dl>

 

 




