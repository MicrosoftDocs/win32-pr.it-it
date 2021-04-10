---
title: attributo char
description: La parola chiave char specifica un elemento di dati a 8 bit.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- attributo char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857593"
---
# <a name="char-attribute"></a>attributo char

La parola chiave **char** specifica un elemento di dati a 8 bit.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome identificatore* 
</dt> <dd>

Specifica un identificatore MIDL valido. Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.

</dd> </dl>

## <a name="remarks"></a>Commenti

La parola chiave **char** identifica un elemento di dati con 8 bit. Al compilatore MIDL, un **carattere** è senza segno per impostazione predefinita ed è sinonimo di [](unsigned.md) **carattere** senza segno.

In questa versione di Microsoft RPC, le tabelle di conversione dei caratteri che eseguono la conversione tra ASCII e EBCDIC sono compilate nelle librerie di runtime e non possono essere modificate dall'utente.

Il tipo **char** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL). Il tipo **char** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro). Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).

I compilatori IDL DCE non accettano la parola chiave [**signed**](signed.md) applicata ai tipi **char** . Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**byte**](byte.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**con segno**](signed.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unsigned**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




