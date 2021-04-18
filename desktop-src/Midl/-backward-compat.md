---
title: /backward_compat opzione
description: Il \_ commutatore di compatibilità/backward indica al compilatore MIDL di disattivare alcune funzionalità avanzate quando generano stub RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297965"
---
# <a name="backward_compat-switch"></a>\_opzione/backward compat

Il \_ commutatore di compatibilità/backward indica al compilatore MIDL di disattivare alcune funzionalità avanzate quando generano stub RPC/com.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Opzioni switch

*\_dimensioni MAYBENULL*<dl> Applica l'attributo [ \[ Disable \_ \_ verifica \] coerenza](disable-consistence-check.md) a un'intera compilazione MIDL.  
</dl>

*azzeramento \_ alignmentgap*<dl> Disattiva lo zero dei gap nel buffer sottoposto a marshalling.  
</dl>

*\_Escape BSTR byValue \_*<dl> Indica al compilatore MIDL di rispettare le sequenze di escape, ad esempio â € ̃ \\ nâ™ o â € ̃ \\ tâ €™ in BSTRS.  
</dl>

*stringa \_ DefaultValue*<dl> Impone al compilatore MIDL di forzare le stringhe negli attributi [**\[ DEFAULTVALUE \]**](defaultvalue.md) in Variant. Tipo di VT \_ I4 prima di assegnare il valore al tipo corretto.  
</dl>

*\_WCHAR \_ t firmato*<dl> Indica a MIDL di considerare il \_ Tipo wchar t come firmato per la compatibilità con Visual Basic.  
</dl>

## <a name="remarks"></a>Commenti

-   *\_ dimensioni MAYBENULL*: vedere \[ disabilitare la \_ Verifica della coerenza \_ \] .
-   *azzeramento \_ alignmentgap*: quando IDLs vengono compilati con la destinazione nt60 o una versione successiva, MIDL creerà gli stub che azzerano i gap di allineamento tra i membri o una struttura nel buffer di transito. L'opzione della riga di comando */Backward \_ compat zero \_ alignmentgap* indirizza MIDL per disabilitare questa funzionalità.

    Nella struttura di esempio seguente, il buffer di trasmissione contiene un gap di allineamento a 7 byte per allineare il membro Hyper a 8 dopo il membro Char. Con la destinazione NT60 o versione successiva, MIDL Azzera tale gap a meno che non venga usata l'opzione.

    File IDL:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Questa opzione può offrire un lieve miglioramento delle prestazioni con un aumento potenzialmente significativo del rischio di divulgazione.

-   *\_ \_ Escape di BSTR byValue*: per impostazione predefinita, il compilatore MIDL non elabora sequenze di escape, ad esempio â € ̃ \\ NÂ™ o â € ̃ \\ tâ €™ nelle costanti di stringa per l'automazione OLE durante la conversione di una costante di stringa nei tipi VT \_ LPSTR o VT \_ LPWSTR. Con questa opzione per la compatibilità con le versioni precedenti, vengono valutate le sequenze di escape.
-   *String \_ DefaultValue*: impone al compilatore MIDL di assegnare le stringhe numeriche negli attributi [**\[ \] DefaultValue**](defaultvalue.md) a Variant. Tipo di VT \_ I4 prima di assegnare il valore al tipo corretto. Questo può causare una perdita di precisione in alcuni casi, pertanto questa opzione non è consigliata.
-   con *segno \_ WCHAR \_ t*: indica a MIDL di considerare il \_ Tipo wchar t come firmato per la compatibilità con Visual Basic.

 

 




