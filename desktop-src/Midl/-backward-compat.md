---
title: Opzione /backward_compat
description: L'opzione /backward compat indica al compilatore MIDL di disattivare alcune funzionalità avanzate \_ durante la generazione di stub RPC/COM.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd412bdabe4255a9a4538503b29ddf5681265ce5e16c81d3d5fc2484eb6c9675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086391"
---
# <a name="backward_compat-switch"></a>Opzione /backward \_ compat

L'opzione /backward compat indica al compilatore MIDL di disattivare alcune funzionalità avanzate \_ durante la generazione di stub RPC/COM.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Opzioni switch

*maybenull \_ sizeis*<dl> Applica [ \[ \_ l'attributo disable consistency \_ check \] ](disable-consistence-check.md) a un'intera compilazione MIDL.  
</dl>

*zeroout \_ alignmentgap*<dl> Disattiva l'azzeramento degli spazi nel buffer sottoposto a marshalling.  
</dl>

*Escape \_ BSTR per \_ valore*<dl> Indica al compilatore MIDL di rispettare le sequenze di escape, ad esempio â€ \\ nâ€™ o â€ â€ \\ tâ€™ in BSTR.  
</dl>

*string \_ defaultvalue*<dl> Forza il compilatore MIDL a forzare le stringhe negli [**\[ attributi defaultvalue \]**](defaultvalue.md) in VARIANT. Tipo VT \_ I4 prima di forzare il valore nel tipo corretto.  
</dl>

*signed \_ wchar \_ t*<dl> Indica a MIDL di considerare il tipo wchar \_ t come firmato per garantire la compatibilità con Visual Basic.  
</dl>

## <a name="remarks"></a>Commenti

-   *maybenull \_ sizeis:* vedere \[ Disabilitare \_ la verifica \_ \] coerenza.
-   *zeroout \_ alignmentgap:* quando gli IDL vengono compilati con NT60 o versione successiva di destinazione, MIDL crea stub che azzerino eventuali spazi di allineamento tra i membri o una struttura nel wire buffer. L'opzione della riga *di comando /backward \_ compat zeroout \_ alignmentgap* indica a MIDL di disabilitare questa funzionalità.

    Nella struttura di esempio seguente il buffer di collegamento contiene un gap di allineamento di 7 byte per allineare il membro hyper a 8 dopo il membro char. Con NT60 di destinazione o superiore, MIDL azzererà tale gap a meno che non venga usata l'opzione .

    File IDL:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Questa opzione può offrire un leggero miglioramento delle prestazioni con un aumento potenzialmente significativo del rischio di divulgazione.

-   Escape BSTR per valore: per impostazione predefinita, il compilatore MIDL non elabora sequenze di escape come â€ *\_ \_* \\ nâ€ nâ€™ o â€ tâ€ tâ€™ nelle costanti stringa per Automazione OLE durante la conversione di una costante stringa nei tipi \\ VT LPSTR o \_ \_ VT LPWSTR. Con questa opzione di opzione di compatibilità con le versioni precedenti, vengono valutate le sequenze di escape.
-   *string \_ defaultvalue:* forza il compilatore MIDL a forzare le stringhe numeriche negli [**\[ attributi defaultvalue \]**](defaultvalue.md) in VARIANT. Tipo VT \_ I4 prima di forzare il valore nel tipo corretto. Ciò può causare una perdita di precisione in alcuni casi, quindi questa opzione switch non è consigliata.
-   *signed \_ wchar \_ t:* indica a MIDL di considerare il tipo wchar t come \_ firmato per compatibilità con Visual Basic.

 

 




