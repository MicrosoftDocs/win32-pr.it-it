---
description: Definisce diritti standard, specifici e generici. Questi diritti vengono usati nelle voci di controllo di accesso (ACE) e sono il mezzo principale per specificare l'accesso richiesto o concesso a un oggetto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13378b44d17bedd818efd5fc84310b304a2f683a3331237e8cca208be8de810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785468"
---
# <a name="access_mask"></a>MASCHERA DI \_ ACCESSO

Il **tipo di dati ACCESS \_ MASK** è un **valore DWORD** che definisce diritti standard, specifici e generici. Questi diritti vengono usati nelle voci di [*controllo*](/windows/desktop/SecGloss/a-gly) di accesso (ACE) e sono il mezzo principale per specificare l'accesso richiesto o concesso a un oggetto.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Commenti

I bit in questo valore vengono allocati come indicato di seguito.



| BITS             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Diritti specifici. Contiene la maschera di accesso specifica del tipo di oggetto associato alla maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Diritti standard. Contiene i diritti di accesso standard dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Accedere alla sicurezza del sistema (**ACCESS \_ SYSTEM \_ SECURITY**). Viene usato per indicare l'accesso a un elenco [*di controllo di accesso*](/windows/desktop/SecGloss/s-gly) di sistema (SACL). Questo tipo di accesso richiede che il processo chiamante abbia il edizione Standard **\_ SECURITY \_ NAME** (Manage auditing and security log). Se questo flag è impostato nella maschera di accesso di una voce di controllo di accesso (accesso riuscito o non riuscito), l'accesso SACL verrà eseguito.<br/> |
| 25<br/>    | Massimo consentito (**MAXIMUM \_ ALLOWED**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Riservato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Generic all (**GENERIC \_ ALL**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Esecuzione generica (**GENERIC \_ EXECUTE**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Scrittura generica (**GENERIC \_ WRITE**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Lettura generica (**GENERIC \_ READ**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

I bit dei diritti standard, da 16 a 23, contengono i diritti di accesso standard dell'oggetto e possono essere una combinazione dei flag predefiniti seguenti.



| bit           | Contrassegno                         | Significato                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Eliminare l'accesso.<br/>                                                                                                                                                                                                                |
| 17<br/> | **CONTROLLO \_ LETTURA**<br/> | Accesso in lettura al proprietario, al gruppo e [*all'elenco*](/windows/desktop/SecGloss/d-gly) di controllo di accesso discrezionale (DACL) del descrittore di sicurezza.<br/> |
| 18<br/> | **APPLICAZIONE \_ LIVELLO DATI WRITE**<br/>    | Accesso in scrittura all'elenco DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **WRITE \_ OWNER**<br/>  | Accesso in scrittura al proprietario.<br/>                                                                                                                                                                                                        |
| 20<br/> | **Sincronizzare**<br/>   | Sincronizzare l'accesso.<br/>                                                                                                                                                                                                           |



 

Le costanti seguenti definite in Winnt.h rappresentano i diritti di accesso specifici e standard.


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso](access-control.md)
</dt> <dt>

[Strutture di controllo di accesso di base](authorization-structures.md)
</dt> <dt>

[Diritti di accesso e maschere di accesso](access-rights-and-access-masks.md)
</dt> <dt>

[**MAPPING \_ GENERICO**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

