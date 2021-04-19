---
description: Nell'elenco seguente sono elencati i valori possibili del campo Flags in una voce di controllo di accesso (ACE) WMI.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Costanti del flag ACE dello spazio dei nomi (Winnt. h)
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
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331844"
---
# <a name="namespace-ace-flag-constants"></a>Costanti del flag ACE dello spazio dei nomi

Nell'elenco seguente sono elencati i valori possibili del campo **Flags** in una voce di controllo di accesso (ACE) WMI.

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OGGETTO che \_ eredita \_ ACE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Gli oggetti figlio non contenitore ereditano la voce ACE come una voce ACE efficace.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**il contenitore \_ eredita \_ ACE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



La voce ACE ha un effetto sugli spazi dei nomi figlio e sullo spazio dei nomi corrente.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**Nessuna \_ propagazione \_ eredita \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



La voce ACE si applica solo allo spazio dei nomi corrente e agli elementi figlio immediati.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**EREDITA \_ solo \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



La voce ACE si applica solo agli spazi dei nomi figlio.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**Ace EREDITAta \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Questa impostazione non viene impostata dai client, ma viene segnalata ai client quando l'origine di una voce ACE è uno spazio dei nomi padre.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sicurezza WMI](wmi-security-constants.md)
</dt> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Definizione dell'ereditarietà della sicurezza dello spazio dei nomi](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




