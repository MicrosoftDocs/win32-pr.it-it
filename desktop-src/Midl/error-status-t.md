---
title: attributo error_status_t
description: La \_ \_ parola chiave Error Status t designa un tipo per un oggetto che contiene informazioni sullo stato di comunicazione o sugli errori.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- attributo error_status_t MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333583"
---
# <a name="error_status_t-attribute"></a>\_attributo stato errore \_ t

La parola chiave **Error \_ status \_ t** designa un tipo per un oggetto che contiene informazioni sullo stato di comunicazione o sugli errori.

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF, ad esempio **\[** [**\_ stato di comunicazione**](comm-status.md) **\]** , **\[** [**\_ stato di errore**](fault-status.md) **\]** o **\[** [**NoCode**](nocode.md) **\]** . Gli attributi della funzione sono racchiusi tra parentesi quadre. È possibile applicare zero o più attributi a una funzione. Separare più attributi di funzione con virgole.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parametri-attributi* 
</dt> <dd>

Specifica gli attributi che si applicano a un parametro. Si noti che è possibile applicare zero, uno o più attributi al parametro. Separare più attributi di parametro con virgole. Gli attributi di parametro sono racchiusi tra parentesi quadre. Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica il parametro per la funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo di **stato di errore \_ \_ t** viene usato come parte dell'architettura di gestione delle eccezioni in IDL. Questo tipo esegue il mapping a un oggetto [**Long**](long.md) [**senza segno**](unsigned.md) . Le applicazioni che intercettano situazioni di errore presentano un **\[** parametro [**out**](out-idl.md) **\]** o un tipo restituito di una procedura specificata come **stato di errore \_ \_ t** e qualificano lo **stato di errore \_ \_ t** con gli attributi di stato **\[** di [**comunicazione \_**](comm-status.md) o di **\]** **\[** [**\_ stato**](fault-status.md) di errore **\]** in ACF. Se il parametro o il tipo restituito non è stato qualificato con lo **\[ \_ stato \] di comunicazione** o gli attributi di **\[ \_ stato \] di errore** , il parametro funziona come se fosse un long senza segno.

A partire dalla versione 2,0, il compilatore MIDL genera stub che contengono l'architettura di gestione degli errori corretta. Tuttavia, le versioni precedenti del compilatore MIDL gestivano un parametro o un tipo restituito di **stato di errore \_ \_ t** come se **\[** fossero stati applicati lo [**\_ stato di comunicazione**](comm-status.md) **\]** e gli attributi di **\[** [**\_ stato**](fault-status.md) di errore **\]** , anche se non erano. Con MIDL 2,0 o versione successiva, è necessario applicare in modo esplicito gli attributi **\[ \_ stato \] di comunicazione** e **\[ \_ stato \] di errore** al parametro o alla routine in ACF.

Il tipo di **stato di errore \_ \_ t** è uno dei tipi predefiniti del linguaggio di definizione dell'interfaccia. I tipi predefiniti possono apparire come identificatori di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come gli identificatori di tipo Function-return-type o come parametri di tipo).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**stato di comunicazione \_**](comm-status.md)
</dt> <dt>

[**stato di errore \_**](fault-status.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> </dl>

 

 




