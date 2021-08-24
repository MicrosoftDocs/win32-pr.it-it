---
title: Risorsa RCDATA
description: Definisce una risorsa dati non elaborati per un'applicazione. Le risorse dati non elaborati consentono l'inclusione di dati binari direttamente nel file eseguibile.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menu delle risorse RCDATA e altre risorse
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f813bde1195d8adcad708c40857cc11b1e7b70f696455168e174a4bf2f6cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847041"
---
# <a name="rcdata-resource"></a>Risorsa RCDATA

Definisce una risorsa dati non elaborati per un'applicazione. Le risorse dati non elaborati consentono l'inclusione di dati binari direttamente nel file eseguibile.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*Nameid*
</dt> <dd>

Nome univoco o valore intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*istruzioni facoltative*
</dt> <dd>

Questo parametro può essere zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Informazioni definite dall'utente su una risorsa che possono essere usate dagli strumenti che leggono e scrivono file di risorse. Per altre informazioni, vedere [**CHARACTERISTICS.**](characteristics-statement.md) |
| [**LINGUA**](language-statement.md) *,* *sottolinguaggio* | Lingua per la risorsa. Per altre informazioni, vedere [**LANGUAGE**](language-statement.md).                                                                                            |
| [**VERSION**](version-statement.md) *dword*                     | Numero di versione definito dall'utente per la risorsa che può essere usato dagli strumenti che leggono e scrivono file di risorse. Per altre informazioni, vedere [**VERSION.**](version-statement.md)              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dati non elaborati*
</dt> <dd>

Dati non elaborati costituiti da uno o più numeri interi o stringhe di caratteri. I numeri interi possono essere specificati in formato decimale, ottale o esadecimale. Per essere compatibili con le versioni a 16 bit Windows, i numeri interi vengono archiviati come **valori WORD.** È possibile archiviare un numero intero **come valore DWORD** qualificando l'intero con il suffisso "L".

Le stringhe sono racchiuse tra virgolette. RC non aggiunge automaticamente un carattere Null di terminazione a una stringa. Ogni stringa è una sequenza dei caratteri ANSI specificati, a meno che non venga qualificata come stringa di caratteri wide con il prefisso L.

Il blocco di dati inizia su un limite **DWORD** e RC non esegue la spaziatura interna o l'allineamento dei dati all'interno del *blocco di dati non* elaborati. È responsabilità dell'utente garantire il corretto allineamento dei dati all'interno del blocco.

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse.](common-resource-attributes.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo **dell'istruzione RCDATA:**

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

[**Acceleratori**](accelerators-resource.md)
</dt> <dt>

[**Caratteristiche**](characteristics-statement.md)
</dt> <dt>

[**Lingua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 




