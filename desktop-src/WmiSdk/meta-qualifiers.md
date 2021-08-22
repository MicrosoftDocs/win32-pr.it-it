---
description: I meta qualificatori perfezionano la definizione di meta-costrutti nel modello CIM chiarendo l'utilizzo effettivo di una dichiarazione di classe o di proprietà all'interno della sintassi MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Qualificatori di metadati
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76609fecca3e3831372ea813e7210cd449c2e1e4fc527df605bc523efd4c1be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131178"
---
# <a name="meta-qualifiers"></a>Qualificatori di metadati

I meta qualificatori perfezionano la definizione di meta-costrutti nel modello CIM chiarendo l'utilizzo effettivo di una dichiarazione di classe o di proprietà all'interno della sintassi MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Associazione**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi

Indica se la classe è una classe di associazione utilizzata per descrivere una relazione tra altre due classi. L'assenza di questo qualificatore indica che la classe non è una classe di associazione. Questo qualificatore si escludono a vicenda con **l'indicazione**. Per altre informazioni, vedere [Dichiarazione di una classe di associazione](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicazione**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi

Indica se la classe di oggetti definisce un'indicazione. Questo qualificatore si escludono a vicenda con **Association**. Il valore predefinito è **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Qualificatori WMI](wmi-qualifiers.md)
</dt> <dt>

[Aggiunta di un qualificatore](adding-a-qualifier.md)
</dt> </dl>

 

 




