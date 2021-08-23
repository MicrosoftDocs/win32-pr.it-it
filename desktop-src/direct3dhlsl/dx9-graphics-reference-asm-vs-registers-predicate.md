---
title: Registro predicati (informazioni di riferimento su HLSL VS)
description: Questo registro di output vertex shader contiene un valore booleano per canale.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28392f7bb9c2f59bd766e42ec21fb87a854b08bedd8336ebb6f7249b7eccb940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119575"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Registro predicati (informazioni di riferimento su HLSL VS)

Questo registro di output vertex shader contiene un valore booleano per canale.

Un registro predicato è supportato dalle versioni seguenti.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| registro di predicati     |      |      |       | x    | x    | x     |



 

Ecco le proprietà del registro.



| Tipo di registrazione | Conteggio | L/S | \# Leggere le porte | \# Reads/inst | Dimensione | RelAddr | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicato(p)  | 1     | L/S | 1             | 1             | 4         | N/A     | Nessuno     | N            |



 

Il registro del predicato può essere modificato con [setp \_ comp - rispetto a](setp-comp---vs.md). Non sono presenti valori predefiniti per questo registro. Un'applicazione deve impostare il registro prima di essere usato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




