---
description: Specifica un certificato utilizzato per firmare un documento. Il certificato può essere archiviato in un file SPC (Software Publisher Certificate) o in un archivio certificati.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: d31670575db045430e78b6c6b3182f4561b0d4784c1e1c0da95ff8629154d2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898874"
---
# <a name="signer_cert-structure"></a>Struttura DEL \_ CERTIFICATO DEL FIRMATARIO

La **struttura SIGNER \_ CERT** specifica un [*certificato usato*](../secgloss/c-gly.md) per firmare un documento. Il certificato può essere archiviato in un file [*SPC (Software Publisher Certificate)*](../secgloss/s-gly.md) o in un [*archivio certificati*](../secgloss/c-gly.md).

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura .

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Specifica la modalità di archiviazione del certificato. Questo membro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**FIRMATARIO \_ CERT \_ SPC \_ FILE**</dt> <dt>1</dt> </dl>    | Il certificato viene archiviato in un file SPC. Il **membro pwszSpcFile** contiene il percorso e il nome file del file SPC.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**FIRMATARIO \_ CERT \_ STORE**</dt> <dt>2</dt> </dl>              | Il certificato viene archiviato in un archivio certificati. Il **membro pCertStoreInfo** contiene un puntatore a una struttura [**SIGNER \_ CERT STORE \_ \_ INFO**](signer-cert-store-info.md) che specifica l'archivio certificati in cui è archiviato il certificato.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**FIRMATARIO \_ CERT \_ SPC \_ CHAIN**</dt> <dt>3</dt> </dl> | Il certificato viene archiviato in un file SPC ed è associato a una catena di certificati. Il **membro pSpcChainInfo contiene** un puntatore a una struttura [**SIGNER \_ SPC CHAIN \_ \_ INFO**](signer-spc-chain-info.md) che contiene le informazioni sulla catena per il certificato.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che contiene il percorso e il nome file del file SPC in cui è archiviato il certificato. Questo membro viene usato solo se il **membro dwCertChoice** contiene **SIGNER \_ CERT \_ SPC \_ FILE**.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Puntatore a una [**struttura \_ SIGNER CERT \_ STORE \_ INFO**](signer-cert-store-info.md) che specifica l'archivio certificati in cui è archiviato il certificato. Questo membro viene usato solo se il **membro dwCertChoice** contiene **SIGNER \_ CERT \_ STORE.**

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Puntatore a una [**struttura SIGNER \_ SPC \_ CHAIN \_ INFO**](signer-spc-chain-info.md) che contiene le informazioni sulla catena per il certificato. Questo membro viene usato solo se il **membro dwCertChoice** contiene **SIGNER \_ CERT \_ SPC \_ CHAIN.**

</dd> <dt>

**Hwnd**
</dt> <dd>

Handle della finestra da utilizzare come proprietario di qualsiasi finestra di dialogo visualizzata. Questo membro non è attualmente utilizzato e viene ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firma del firmatario**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
