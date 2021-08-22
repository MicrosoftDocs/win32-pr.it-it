---
description: Specifica il provider del servizio di crittografia (CSP) e le informazioni sulla chiave privata utilizzate per creare una firma digitale.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 45ab23e4a568082de7e7fb4d23364ac6ba15c0f61378d54735cbc398e7e0e8ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898688"
---
# <a name="signer_provider_info-structure"></a>Struttura DELLE INFORMAZIONI \_ \_ SUL PROVIDER DI FIRMATARI

La **struttura SIGNER \_ PROVIDER \_ INFO** specifica il [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) e le informazioni sulla chiave privata usate per creare una firma digitale.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla manualmente come illustrato in questo argomento.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione, in byte, della struttura .

</dd> <dt>

**pwszProviderName**
</dt> <dd>

Nome del provider di servizi di rete utilizzato per creare la firma digitale. Se il valore di questo membro è **NULL,** viene usato il provider predefinito.

</dd> <dt>

**dwProviderType**
</dt> <dd>

Tipo del provider di servizi di configurazione specificato dal **membro pwszProviderName.**

</dd> <dt>

**dwKeySpec**
</dt> <dd>

Specifica delle chiavi. Se questo membro è impostato su zero, viene usata la specifica della chiave nel membro **pwszPvkFileName** o **pwszKeyContainer.** Se è presente più di una specifica di chiave nel **membro pwszKeyContainer,** viene usato **AT \_ SIGNATURE.** Se non riesce, **viene usato AT \_ KEYEXCHANGE.**

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Specifica il tipo di informazioni sulla chiave privata. Questo membro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                               | Significato                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ DIGITARE \_ NOME \_ FILE**</dt> <dt>1 (0x1)</dt> </dl>         | Le informazioni sulla chiave privata sono un nome file.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ TYPE \_ KEYCONTAINER**</dt> <dt>2 (0x2)</dt> </dl> | Le informazioni sulla chiave privata sono un contenitore di chiavi.<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

Nome del file che contiene le informazioni sulla chiave privata.

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

Nome del contenitore di chiavi che contiene le informazioni sulla chiave privata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
