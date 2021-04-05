---
description: Specifica un certificato del server di pubblicazione software (SPC) e una catena di certificati utilizzati per firmare un documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Struttura SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131650"
---
# <a name="signer_spc_chain_info-structure"></a>Struttura delle \_ \_ informazioni sulla catena \_ di firma SPC

La struttura **\_ \_ \_ info Chain SPC del firmatario** specifica un [*certificato dell'editore del software*](../secgloss/s-gly.md) (SPC) e una catena di certificati usati per firmare un documento.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Nome del file SPC da usare per firmare un documento.

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

 

 
