---
description: Specifica un certificato utilizzato per firmare un documento. Il certificato può essere archiviato in un file di certificato dell'editore del software (SPC) o in un archivio certificati.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Struttura SIGNER_CERT
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
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233123"
---
# <a name="signer_cert-structure"></a>Struttura del certificato del FIRMATARIo \_

La struttura del certificato del **firmatario \_** specifica un [*certificato*](../secgloss/c-gly.md) utilizzato per firmare un documento. Il certificato può essere archiviato in un file di [*certificato dell'editore del software*](../secgloss/s-gly.md) (SPC) o in un [*archivio certificati*](../secgloss/c-gly.md).

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

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

Dimensione, in byte, della struttura.

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Specifica la modalità di archiviazione del certificato. Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**\_ Firmatario \_ \_ File di certificato SPC**</dt> <dt>1</dt> </dl>    | Il certificato viene archiviato in un file SPC. Il membro **pwszSpcFile** contiene il percorso e il nome file del file SPC.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**\_ Firmatario \_Archivio certificati**</dt> <dt>2</dt> </dl>              | Il certificato viene archiviato in un archivio certificati. Il membro **pCertStoreInfo** contiene un puntatore a una struttura di informazioni dell'archivio certificati del firmatario che specifica l'archivio certificati in cui è archiviato il certificato. [**\_ \_ \_**](signer-cert-store-info.md)<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**\_ Firmatario \_ \_ Catena di certificati SPC**</dt> <dt>3</dt> </dl> | Il certificato viene archiviato in un file SPC ed è associato a una catena di certificati. Il membro **pSpcChainInfo** contiene un puntatore a una struttura di informazioni della [**catena di SPC del firmatario \_ \_ \_**](signer-spc-chain-info.md) che contiene le informazioni sulla catena per il certificato.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che contiene il percorso e il nome file del file SPC in cui è archiviato il certificato. Questo membro viene utilizzato solo se il membro **dwCertChoice** contiene il **\_ \_ \_ file SPC del certificato del firmatario**.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Puntatore a una struttura di [**\_ \_ \_ informazioni dell'archivio certificati del firmatario**](signer-cert-store-info.md) che specifica l'archivio certificati in cui è archiviato il certificato. Questo membro viene usato solo se il membro **dwCertChoice** contiene l' **\_ \_ Archivio del certificato del firmatario**.

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Puntatore a una struttura di [**\_ \_ \_ informazioni della catena SPC del firmatario**](signer-spc-chain-info.md) che contiene le informazioni sulla catena per il certificato. Questo membro viene usato solo se il membro **dwCertChoice** contiene una **\_ \_ \_ catena di certificati SPC del firmatario**.

</dd> <dt>

**HWND**
</dt> <dd>

Handle della finestra da utilizzare come proprietario di tutte le finestre di dialogo visualizzate. Questo membro non è attualmente in uso e viene ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
