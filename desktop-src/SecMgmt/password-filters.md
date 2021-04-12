---
description: Filtri password
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtri password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233682"
---
# <a name="password-filters"></a>Filtri password

I filtri password consentono di implementare i criteri password e le notifiche di modifica.

Quando viene effettuata una richiesta di modifica della password, l' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) chiama i filtri password registrati nel sistema. Ogni filtro password viene chiamato due volte: prima per convalidare la nuova password e quindi, dopo che tutti i filtri hanno convalidato la nuova password, per notificare ai filtri che è stata apportata la modifica. Questo processo viene illustrato nella figura seguente.

![richiesta di modifica della password](images/pswdfilte.png)

La notifica di modifica della password viene usata per sincronizzare le modifiche delle password con i database degli account esterni.

I filtri password vengono usati per applicare i criteri password. I filtri convalidano le nuove password e indicano se la nuova password è conforme ai criteri di password implementati.

Per una panoramica dell'uso dei filtri password, vedere [using password filters](using-password-filters.md).

Per un elenco delle funzioni di filtro delle password, vedere [funzioni di filtro delle password](management-functions.md).

Negli argomenti seguenti vengono fornite ulteriori informazioni sui filtri password:

-   [Considerazioni sulla programmazione del filtro password](password-filter-programming-considerations.md)
-   [Imposizione avanzata delle password e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
