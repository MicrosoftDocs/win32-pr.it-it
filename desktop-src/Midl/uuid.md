---
title: uuid (attributo)
description: L'attributo \ UUID \ Interface definisce un identificatore univoco universale (UUID) assegnato all'interfaccia e che lo distingue dalle altre interfacce.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- attributo uuid attributo MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718535"
---
# <a name="uuid-attribute"></a>uuid (attributo)

L'attributo di interfaccia **\[ UUID \]** designa un identificatore univoco universale (UUID) assegnato all'interfaccia e che lo distingue dalle altre interfacce.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*stringa-UUID* 
</dt> <dd>

Specifica una stringa costituita da 8 cifre esadecimali seguite da un trattino, quindi da tre gruppi di 4 cifre esadecimali seguite da un trattino e quindi da 12 cifre esadecimali. È possibile racchiudere la stringa UUID tra virgolette, tranne quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La libreria di runtime utilizza l'UUID dell'interfaccia che l'attributo **\[ UUID \]** designa per stabilire la comunicazione tra le applicazioni client e server. L'attributo **\[ UUID \]** può essere visualizzato nell'elenco di attributi di interfaccia per un'interfaccia RPC o un'interfaccia com.

Per un'interfaccia RPC, è necessario che l'elenco di attributi di interfaccia includa l'attributo **\[ UUID \]** o l' **\[** attributo [**local**](local.md) e che quello scelto venga **\]** eseguito esattamente una volta. Se l'elenco include l'attributo **\[ UUID \]** , può includere anche l'attributo **\[** [**Version**](version.md) **\]** .

Per un'interfaccia COM (identificata dall' **\[** [](object.md) **\]** attributo dell'interfaccia oggetto), l'elenco di attributi di interfaccia deve includere l'attributo **\[ UUID \]** , ma non può includere l'attributo **\[ version \]** . L'elenco di un'interfaccia COM può includere l'attributo **\[ locale \]** anche se è presente l'attributo **\[ UUID \]** .

Microsoft RPC supporta un'estensione di DCE IDL che consente di racchiudere l'UUID tra virgolette doppie ("" ""). Il formato racchiuso tra virgolette è necessario per i preprocessori del compilatore C che interpretano i numeri UUID come numeri a virgola mobile.

Tutti i valori UUID devono essere generati dal computer per garantire l'univocità. Usare l'utilità uuidgen per generare valori UUID univoci.

I numeri di versione e UUID dell'interfaccia vengono usati per determinare se il client può essere associato al server. Affinché il client venga associato al server, l'UUID specificato nelle interfacce client e server deve essere lo stesso.

Si noti che un'interfaccia senza attributi può essere importata in un file IDL di base. Tuttavia, l'interfaccia deve contenere solo tipi di oggetto senza procedure. Se nell'interfaccia è inclusa anche una routine, è necessario specificare un attributo local o UUID.

## <a name="examples"></a>Esempi

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 




