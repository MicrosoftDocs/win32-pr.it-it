---
description: I qualificatori di metadati perfezionano la definizione dei metacostrutti nel modello CIM chiarendo l'utilizzo effettivo di una classe o di una dichiarazione di proprietà all'interno della sintassi MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Qualificatori meta
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314593"
---
# <a name="meta-qualifiers"></a>Qualificatori meta

I qualificatori di metadati perfezionano la definizione dei metacostrutti nel modello CIM chiarendo l'utilizzo effettivo di una classe o di una dichiarazione di proprietà all'interno della sintassi MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Associazione**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica se la classe è una classe di associazione utilizzata per descrivere una relazione tra altre due classi. L'assenza di questo qualificatore indica che la classe non è una classe di associazione. Questo qualificatore si escludono a vicenda con l' **indicazione**. Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicazione**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica se la classe di oggetti definisce un'indicazione. Questo qualificatore si escludono a vicenda con **Association**. Il valore predefinito è **false**.

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

 

 




