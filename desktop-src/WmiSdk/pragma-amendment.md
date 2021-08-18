---
description: Indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e specifiche del linguaggio.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: pragma amendment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6204ac7f3cd78de8d2eed9740fc165475d387e65284bcbf6be1ea10ed91a0926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992731"
---
# <a name="pragma-amendment"></a>pragma amendment

Il **comando del** preprocessore pragma amendment indica al compilatore MOF di separare un file MOF in versioni indipendenti dal linguaggio e specifiche del linguaggio. Il file MOF specifico della lingua sposta i qualificatori modificati in uno spazio dei nomi per impostazioni locali specifiche. Compilare quindi i file MOF specifici del linguaggio e indipendenti dalla lingua per archiviare le informazioni sulle classi nel repository WMI.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come creare un file MOF contenente qualificatori modificati. È quindi possibile compilare il codice MOF con il comando seguente:

**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**

Il comando indica al compilatore MOF di produrre due file MOF dal file Mastermof.mof originale. Il compilatore MOF produce una versione indipendente dal linguaggio del file MOF, denominata Lnmof.mof, con tutti gli elementi specifici del linguaggio rimossi. Il compilatore crea anche un secondo file MOF specifico del linguaggio denominato Lsmof.mfl che contiene solo gli elementi che è necessario localizzare.

> [!Note]  
> Quando si suddivide un file MOF con il qualificatore di modifica o il **comando pragma amendment,** è necessario specificare le opzioni **-MOF** e **-MFL.**  In caso contrario, il compilatore non genera alcun file di output. È quindi necessario compilare i due file di output per rendere disponibili le informazioni sulla classe per WMI.

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




