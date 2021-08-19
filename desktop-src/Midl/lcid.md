---
title: Attributo lcid
description: L'attributo \ lcid\ specifica un identificatore delle impostazioni locali e abilita il supporto del compilatore MIDL specifico delle impostazioni locali.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- Attributo lcid MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87d1b6105d7e6ae561d7409cbf256b67f965c61e235ffc5782594cb5623497c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806797"
---
# <a name="lcid-attribute"></a>Attributo lcid

**\[ L'attributo \] lcid** specifica un identificatore delle impostazioni locali e abilita il supporto del compilatore MIDL specifico delle impostazioni locali.

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

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**libreria**](library.md).

</dd> <dt>

*Localeid* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali a 32 bit usato Windows supporto lingua nazionale. In genere l'identificatore delle impostazioni locali è specificato in formato esadecimale.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Zero o più attributi da applicare alla [**libreria**](library.md).

</dd> <dt>

*library-name* 
</dt> <dd>

Nome con cui i componenti software fanno riferimento alla [**libreria**](library.md).

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Una o più istruzioni MIDL che definiscono il contenuto della [**libreria**](library.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione nel file IDL.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati al parametro della funzione.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica il nome del parametro nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\[ sintassi \] lcid** ha due forme diverse. L'effetto dell'attributo dipende dalla sintassi utilizzata, ovvero la sintassi dell'istruzione [**della**](library.md) libreria o la sintassi dei parametri.

Se applicato all'istruzione [**library,**](library.md) insieme a un argomento localeID, come illustrato nel primo esempio, l'attributo **\[ lcid \]** identifica le impostazioni locali per una libreria dei tipi o per un argomento di funzione e consente di usare caratteri internazionali all'interno del blocco della libreria.

Efficace con la versione 3.01.75 del compilatore MIDL, l'identificatore delle impostazioni locali fornito da questo attributo non solo decora la libreria dei tipi risultante, ma modifica effettivamente il comportamento del compilatore. [**All'interno di un'istruzione**](library.md) library, dal punto in cui viene usato l'attributo **\[ lcid, \]** MIDL accetterà l'input localizzato in base alle impostazioni locali specificate. In particolare, è disponibile il supporto completo per le lingue asiatiche, ad esempio giapponese, cinese e coreano (supporto DBCS completo). Le funzionalità supportate dalla localizzazione sono: commenti, stringhe, helpstring e identificatori.

Usare [**l'opzione del**](-lcid.md) compilatore /lcid per avere questo supporto di localizzazione disponibile per l'intero file di input, inclusi il nome file e il percorso della directory, anziché solo all'interno del blocco di libreria.

Quando viene applicato a un parametro, l'attributo **\[ lcid \]** consente di passare un identificatore delle impostazioni locali a una funzione, come illustrato nel secondo esempio. Ai parametri **\[ lcid \]** si applicano le restrizioni seguenti:

-   Una funzione può avere al massimo un **\[ parametro lcid. \]**
-   Il tipo di dati del parametro deve essere [**long**](long.md).
-   La direzione del parametro deve essere **\[** [**solo in**](in.md) **\]** .
-   Il **\[ parametro \] lcid** deve seguire qualsiasi altro parametro, ad eccezione di **\[** [**un parametro retval.**](retval.md) **\]**
-   Non è possibile applicare **\[ l'attributo \] lcid** a un [**parametro di interfaccia dispatch**](dispinterface.md) o [**coclasse.**](coclass.md)

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

[**/lcid**](-lcid.md)
</dt> <dt>

[**Libreria**](library.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 