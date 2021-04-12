---
title: /app_config opzione
description: L'opzione di configurazione/app \_ Seleziona la modalità di configurazione dell'applicazione, che consente di usare alcune parole chiave di ACF nel file IDL. Con questa opzione del compilatore MIDL è possibile omettere l'ACF e specificare un'interfaccia in un unico file IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config switch MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397887"
---
# <a name="app_config-switch"></a>\_opzione di configurazione/app

L' **opzione \_ di configurazione/app** seleziona la modalità di configurazione dell'applicazione, che consente di usare alcune parole chiave di ACF nel file IDL. Con questa opzione del compilatore MIDL è possibile omettere l'ACF e specificare un'interfaccia in un unico file IDL.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Microsoft RPC supporta l'utilizzo degli attributi ACF seguenti nel file IDL:

-   Handle implicito \_
-   \_Handle automatico
-   Handle esplicito \_

Le versioni future di Microsoft RPC possono supportare l'utilizzo di altri attributi ACF nel file IDL. L'opzione di **\_ configurazione/app** rappresenta un'estensione Microsoft per la specifica OSF-DCE e, di conseguenza, si escludono a vicenda con l'opzione [**/OSF**](-osf.md) .

Per ulteriori informazioni relative all'opzione **di \_ configurazione/app** , vedere file di [configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md) e file di [definizione di interfaccia (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Esempio

**nome file di MIDL/app \_ config. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




