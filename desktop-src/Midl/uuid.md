---
title: uuid (attributo)
description: L'attributo di interfaccia \uuid\ definisce un identificatore univoco universale (UUID) assegnato all'interfaccia e che lo distingue dalle altre interfacce.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- Attributo uuid MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce85ad2014e1f0563e2c20af7abec3cc476fab330b38340162f28fd390a5f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066641"
---
# <a name="uuid-attribute"></a>uuid (attributo)

L'attributo di interfaccia **\[ uuid \]** definisce un identificatore univoco universale (UUID) assegnato all'interfaccia e che lo distingue da altre interfacce.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*string-uuid* 
</dt> <dd>

Specifica una stringa costituita da 8 cifre esadecimali seguite da un trattino, quindi tre gruppi di 4 cifre esadecimali, ognuno seguito da un trattino e quindi da 12 cifre esadecimali. È possibile racchiudere la stringa UUID tra virgolette, tranne quando si usa l'opzione del compilatore MIDL [**/osf**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La libreria di runtime usa l'UUID dell'interfaccia designato dall'attributo **\[ uuid \]** per stabilire la comunicazione tra le applicazioni client e server. **\[ L'attributo \] uuid** può essere visualizzato nell'elenco degli attributi dell'interfaccia per un'interfaccia RPC o COM.

Per un'interfaccia RPC, l'elenco di attributi dell'interfaccia deve includere l'attributo **\[ uuid \]** o l'attributo locale e quello scelto deve essere eseguito **\[** [](local.md) **\]** esattamente una volta. Se l'elenco include **\[ l'attributo uuid, \]** può includere anche l'attributo **\[** [**version.**](version.md) **\]**

Per un'interfaccia COM (identificata dall'attributo dell'interfaccia oggetto), l'elenco di attributi dell'interfaccia deve includere l'attributo **\[** [](object.md) **\]** **\[ uuid, \]** ma non può includere **\[ l'attributo version. \]** L'elenco per un'interfaccia COM può includere **\[ l'attributo \]** locale anche se **\[ l'attributo uuid \]** è presente.

Microsoft RPC supporta un'estensione al linguaggio IDL DCE che consente di racchiudere l'UUID tra virgolette doppie ("" ""). Il formato tra virgolette è necessario per i preprocessori del compilatore C che interpretano i numeri UUID come numeri a virgola mobile.

Tutti i valori UUID devono essere generati dal computer per garantire l'univocità. Usare l'utilità Uuidgen per generare valori UUID univoci.

L'UUID e i numeri di versione dell'interfaccia vengono usati per determinare se il client può eseguire l'associazione al server. Per l'associazione del client al server, l'UUID specificato nelle interfacce client e server deve essere lo stesso.

Si noti che un'interfaccia senza attributi può essere importata in un file IDL di base. Tuttavia, l'interfaccia deve contenere solo tipi di dati senza routine. Se nell'interfaccia è contenuta una sola routine, è necessario specificare un attributo locale o UUID.

## <a name="examples"></a>Esempi

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**Oggetto**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 




