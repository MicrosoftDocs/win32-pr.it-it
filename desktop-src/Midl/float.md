---
title: float (attributo)
description: La parola chiave float designa un numero a virgola mobile a 32 bit.
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- attributo float MIDL
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299085"
---
# <a name="float-attribute"></a>float (attributo)

La parola chiave **float** designa un numero a virgola mobile a 32 bit.

``` syntax
float identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo **float** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL). Il tipo **float** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

Il tipo **float** non può essere incluso nelle dichiarazioni [**const**](const.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**doppio**](double.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




