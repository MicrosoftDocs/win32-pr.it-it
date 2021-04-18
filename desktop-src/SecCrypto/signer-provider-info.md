---
description: Specifica le informazioni sul provider del servizio di crittografia (CSP) e sulla chiave privata utilizzate per creare una firma digitale.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Struttura SIGNER_PROVIDER_INFO
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
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316134"
---
# <a name="signer_provider_info-structure"></a>Struttura di \_ informazioni sul provider del firmatario \_

La struttura delle **\_ \_ informazioni del provider del firmatario** specifica le informazioni sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e sulla chiave privata utilizzate per creare una firma digitale.

> [!Note]  
> Questa struttura non è definita in alcun file di intestazione. Per usare questa struttura, è necessario definirla come illustrato in questo argomento.

 

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

Dimensione, in byte, della struttura.

</dd> <dt>

**pwszProviderName**
</dt> <dd>

Nome del CSP utilizzato per creare la firma digitale. Se il valore di questo membro è **null**, viene utilizzato il provider predefinito.

</dd> <dt>

**dwProviderType**
</dt> <dd>

Tipo di CSP specificato dal membro **pwszProviderName** .

</dd> <dt>

**dwKeySpec**
</dt> <dd>

Specifica delle chiavi. Se questo membro è impostato su zero, viene utilizzata la specifica della chiave nel membro **pwszPvkFileName** o **pwszKeyContainer** . Se è presente più di una specifica chiave nel membro **pwszKeyContainer** , viene usata **la \_ firma** . In caso di esito negativo, viene utilizzato il **\_ cambio di** stato.

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Specifica il tipo di informazioni sulla chiave privata. Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                               | Significato                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ Digitare \_ il \_ nome file**</dt> <dt>1 (0x1)</dt> </dl>         | Le informazioni sulla chiave privata sono un nome file.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ TIPO di \_ contenitore di contenitori**</dt> <dt>2 (0x2)</dt> </dl> | Le informazioni sulla chiave privata sono un contenitore di chiavi.<br/> |



 

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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
