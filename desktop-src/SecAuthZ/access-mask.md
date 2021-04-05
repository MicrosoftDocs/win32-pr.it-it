---
description: Definisce diritti standard, specifici e generici. Questi diritti vengono usati nelle voci di controllo di accesso (ACE) e rappresentano il metodo principale per specificare l'accesso richiesto o concesso a un oggetto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131450"
---
# <a name="access_mask"></a>maschera di accesso \_

Il tipo di dati di **Access \_ mask** è un valore **DWORD** che definisce diritti standard, specifici e generici. Questi diritti vengono usati nelle [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) e rappresentano il metodo principale per specificare l'accesso richiesto o concesso a un oggetto.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Commenti

I bit in questo valore vengono allocati come indicato di seguito.



| BITS             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Diritti specifici. Contiene la maschera di accesso specifica per il tipo di oggetto associato alla maschera.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Diritti standard. Contiene i diritti di accesso standard dell'oggetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Accesso alla sicurezza del sistema (**accesso alla \_ \_ sicurezza del sistema**). Viene usato per indicare l'accesso a un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Questo tipo di accesso richiede che il processo chiamante disponga del **privilegio \_ \_ nome sicurezza se** (gestione registro di controllo e di sicurezza). Se questo flag è impostato nella maschera di accesso di una voce di controllo di accesso ACE (accesso con esito positivo o negativo), l'accesso al SACL verrà controllato.<br/> |
| 25<br/>    | Massimo consentito (**massimo \_ consentito**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Riservato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Generic All (**generico \_ All**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Esecuzione generica **( \_ esecuzione generica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Scrittura generica **( \_ scrittura generica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Lettura generica **( \_ lettura generica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

I bit dei diritti standard, da 16 a 23, contengono i diritti di accesso standard dell'oggetto e possono essere costituiti da una combinazione dei flag predefiniti seguenti.



| bit           | Contrassegno                         | Significato                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Elimina accesso.<br/>                                                                                                                                                                                                                |
| 17<br/> | **controllo di lettura \_**<br/> | Accesso in lettura al proprietario, al gruppo e all' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) del descrittore di sicurezza.<br/> |
| 18<br/> | **Scrivi \_ DAC**<br/>    | Accesso in scrittura all'elenco DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **Scrivi \_ proprietario**<br/>  | Accesso in scrittura al proprietario.<br/>                                                                                                                                                                                                        |
| 20<br/> | **SINCRONIZZARE**<br/>   | Sincronizzare l'accesso.<br/>                                                                                                                                                                                                           |



 

Le costanti seguenti definite in Winnt. h rappresentano i diritti di accesso specifici e standard.


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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winnt. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso](access-control.md)
</dt> <dt>

[Strutture di controllo di accesso di base](authorization-structures.md)
</dt> <dt>

[Maschere di accesso e diritti di accesso](access-rights-and-access-masks.md)
</dt> <dt>

[**\_Mapping generico**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

