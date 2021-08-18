---
description: Specifica un certificato SPC (Software Publisher Certificate) e una catena di certificati usati per firmare un documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: SIGNER_SPC_CHAIN_INFO struttura
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
ms.openlocfilehash: ff646da815604082024f7a811f21e786abaece7b8e34944d9bd229c4624ed511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898634"
---
# <a name="signer_spc_chain_info-structure"></a>Struttura SIGNER \_ SPC \_ CHAIN \_ INFO

La **struttura SIGNER \_ SPC CHAIN \_ \_ INFO** specifica un certificato [*SPC (Software Publisher Certificate)*](../secgloss/s-gly.md) e una catena di certificati usati per firmare un documento.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

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

Dimensione, in byte, della struttura .

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Nome del file SPC da usare per firmare un documento.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Specifica la modalità di aggiunta dei certificati alla firma. Per trovare la catena di certificati, vengono controllati gli archivi MY, CA, ROOT e SPC, oltre all'archivio specificato dal membro **hCertStore.** Questo membro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**FIRMATARIO \_ CERT \_ POLICY \_ CHAIN**</dt> <dt>2 (0x2)</dt> </dl>                           | Aggiungere solo i certificati nella catena di certificati.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**FIRMATARIO \_ CERT \_ POLICY CHAIN NO \_ \_ \_ ROOT**</dt> <dt>8 (0x8)</dt> </dl> | Aggiungere solo i certificati nella catena di certificati, escluso il certificato radice.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**FIRMATARIO \_ CERT \_ POLICY \_ STORE**</dt> <dt>1 (0x1)</dt> </dl>                           | Aggiungere tutti i certificati nell'archivio specificato dal **membro hCertStore.** Questo flag può essere una combinazione **OR** bit per bit con qualsiasi altro valore possibile per questo membro.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

facoltativo. Handle per un archivio certificati aggiuntivo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CERTIFICATO DEL \_ FIRMATARIO**](signer-cert.md)
</dt> </dl>

 

 
