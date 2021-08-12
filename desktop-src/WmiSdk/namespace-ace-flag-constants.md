---
description: Nell'elenco seguente sono elencati i valori possibili del campo Flags in una voce di controllo di accesso (ACE) WMI.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Costanti dei flag ACE dello spazio dei nomi (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 7b4051a6c17e9861d656207335b2543cf7d886e74569c269df2a4f680f47fbe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555181"
---
# <a name="namespace-ace-flag-constants"></a>Costanti dei flag ACE dello spazio dei nomi

Nell'elenco seguente sono elencati i valori possibili **del campo Flags** in una voce di controllo di accesso (ACE) WMI.

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Gli oggetti figlio non contenitore ereditano la ACE come ACE effettiva.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



La ACE ha effetto sugli spazi dei nomi figlio e sullo spazio dei nomi corrente.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO \_ PROPAGATE \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



La ACE si applica solo allo spazio dei nomi corrente e agli elementi figlio immediati.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT \_ ONLY \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



La ACE si applica solo agli spazi dei nomi figlio.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**ACE \_ EREDITATO**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Questa impostazione non viene impostata dai client, ma viene segnalata ai client quando l'origine di una ACE è uno spazio dei nomi padre.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Impostazione dei descrittori di sicurezza namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Definizione dell'ereditarietà della sicurezza dello spazio dei nomi](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




