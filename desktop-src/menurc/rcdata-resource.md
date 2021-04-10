---
title: Risorsa RCDATA
description: Definisce una risorsa di dati non elaborati per un'applicazione. Le risorse dei dati non elaborati consentono l'inclusione di dati binari direttamente nel file eseguibile.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menu risorse RCDATA e altre risorse
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103956004"
---
# <a name="rcdata-resource"></a>Risorsa RCDATA

Definisce una risorsa di dati non elaborati per un'applicazione. Le risorse dei dati non elaborati consentono l'inclusione di dati binari direttamente nel file eseguibile.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome univoco o valore Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*
</dt> <dd>

Questo parametro può essere costituito da zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caratteristiche**](characteristics-statement.md) *DWORD*     | Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse. Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md). |
| [](language-statement.md) *Lingua* lingua, *lingua* | Lingua per la risorsa. Per ulteriori informazioni, vedere [**Language**](language-statement.md).                                                                                            |
| [](version-statement.md) *DWORD* versione                     | Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse. Per ulteriori informazioni, vedere [**Version**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dati non elaborati*
</dt> <dd>

Dati non elaborati costituiti da uno o più numeri interi o stringhe di caratteri. I numeri interi possono essere specificati in formato decimale, ottale o esadecimale. Per essere compatibile con Windows a 16 bit, i numeri interi vengono archiviati come valori di **Word** . È possibile archiviare un valore integer come valore **DWORD** qualificando l'Integer con il suffisso "L".

Le stringhe sono racchiuse tra virgolette. RC non aggiunge automaticamente un carattere di terminazione null a una stringa. Ogni stringa è una sequenza dei caratteri ANSI specificati, a meno che non venga qualificata come stringa di caratteri wide con il prefisso L.

Il blocco di dati inizia in un limite **DWORD** e RC non esegue la spaziatura interna o l'allineamento dei dati all'interno del blocco di *dati non elaborati* . È responsabilità dell'utente assicurare l'allineamento corretto dei dati all'interno del blocco.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **RCDATA** :

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 




