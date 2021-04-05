---
title: attributo LCID
description: L'attributo \ LCID \ specifica un identificatore delle impostazioni locali e Abilita il supporto del compilatore MIDL specifico delle impostazioni locali.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- attributo LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725095"
---
# <a name="lcid-attribute"></a>attributo LCID

L'attributo **\[ LCID \]** specifica un identificatore delle impostazioni locali e Abilita il supporto del compilatore MIDL specifico delle impostazioni locali.

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**libreria**](library.md).

</dd> <dt>

*localeID* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali a 32 bit utilizzato nel supporto della lingua nazionale di Windows. In genere l'identificatore delle impostazioni locali viene specificato in formato esadecimale.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Zero o più attributi da applicare alla [**libreria**](library.md).

</dd> <dt>

*nome della libreria* 
</dt> <dd>

Nome con cui i componenti software fanno riferimento alla [**libreria**](library.md).

</dd> <dt>

*Library-Definition-Statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono il contenuto della [**libreria**](library.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati al parametro della funzione.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica il nome del parametro nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi **\[ \] LCID** presenta due forme diverse. l'effetto dell'attributo dipende dalla sintassi utilizzata, ovvero dalla sintassi dell'istruzione [**Library**](library.md) o dalla sintassi dei parametri.

Quando viene applicato all'istruzione [**Library**](library.md) , insieme a un argomento LocaleID, come illustrato nel primo esempio, l'attributo **\[ LCID \]** identifica le impostazioni locali per una libreria dei tipi o per un argomento della funzione e consente di utilizzare caratteri internazionali all'interno del blocco di libreria.

A partire dalla versione 3.01.75 del compilatore MIDL, l'identificatore delle impostazioni locali fornito da questo attributo non solo decora la libreria dei tipi risultante, ma modifica effettivamente il comportamento del compilatore. All'interno di un'istruzione [**Library**](library.md) , dal punto in cui viene usato l'attributo **\[ LCID \]** , MIDL accetterà l'input localizzato in base alle impostazioni locali specificate. In particolare, è disponibile il supporto completo per le lingue asiatiche come il giapponese, il cinese e il coreano (supporto completo DBCS). Le funzionalità supportate dalla localizzazione sono: commenti, stringhe, HelpStrings e identificatori.

Usare l'opzione del compilatore [**/LCID**](-lcid.md) per fare in modo che questo supporto per la localizzazione sia disponibile per l'intero file di input, inclusi il nome file e il percorso della directory, anziché solo all'interno del blocco di libreria.

Quando viene applicato a un parametro, l'attributo **\[ LCID \]** consente di passare un identificatore delle impostazioni locali a una funzione, come illustrato nel secondo esempio. Ai parametri **\[ LCID \]** si applicano le restrizioni seguenti:

-   Una funzione può avere al massimo un parametro **\[ LCID \]** .
-   Il tipo di dati del parametro deve essere [**Long**](long.md).
-   La direzione del parametro deve essere solo **\[** [**in**](in.md) **\]** .
-   Il parametro **\[ LCID \]** deve seguire tutti gli altri parametri, ad eccezione di un **\[** parametro [**retval**](retval.md) **\]** .
-   Non è possibile applicare l'attributo **\[ LCID \]** a un parametro [**Dispatch**](dispinterface.md) o [**coclass**](coclass.md) .

## <a name="examples"></a>Esempi

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/LCID**](-lcid.md)
</dt> <dt>

[**libreria**](library.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 