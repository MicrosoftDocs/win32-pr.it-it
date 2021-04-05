---
description: Indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e dal linguaggio.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: modifica pragma
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
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753698"
---
# <a name="pragma-amendment"></a>modifica pragma

Il comando per il preprocessore **pragma emendamento** indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e dal linguaggio. Il file MOF specifico del linguaggio sposta i qualificatori modificati in uno spazio dei nomi per le impostazioni locali specifiche. Compilare quindi i file MOF specifici della lingua e della lingua per archiviare le informazioni sulle classi nel repository WMI.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come creare un file MOF che contiene qualificatori modificati. È quindi possibile compilare il codice MOF con il comando seguente:

**mofcomp** **-MOF: Lnmof. mof** **-MFL: Lsmof. mfl** **Mastermof. mof**

Il comando indica al compilatore MOF di produrre due file MOF dal file Mastermof. mof originale. Il compilatore MOF produce una versione indipendente dal linguaggio del file MOF, denominata Lnmof. mof, con tutti gli elementi specifici della lingua rimossi. Il compilatore crea anche un secondo file MOF specifico del linguaggio denominato Lsmof. mfl che contiene solo gli elementi che è necessario localizzare.

> [!Note]  
> Quando si suddivide un file MOF con il qualificatore della **modifica** o il comando **pragma emendation** , è necessario specificare le opzioni **-MOF** e **-MFL** . In caso contrario, il compilatore non genera alcun file di output. È quindi necessario compilare i due file di output per rendere disponibili le informazioni sulla classe per WMI.

 


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

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




