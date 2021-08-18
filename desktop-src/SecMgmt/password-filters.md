---
description: Filtri password
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtri password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5771fce0e8cbb2826bcf79344e2813587db6dcedc831d7e879b42ab74698b9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894003"
---
# <a name="password-filters"></a>Filtri password

I filtri password consentono di implementare i criteri password e la notifica delle modifiche.

Quando viene effettuata una richiesta [](/windows/desktop/SecGloss/l-gly) di modifica della password, l'autorità di sicurezza locale (LSA) chiama i filtri password registrati nel sistema. Ogni filtro password viene chiamato due volte: prima per convalidare la nuova password e quindi, dopo che tutti i filtri hanno convalidato la nuova password, per notificare ai filtri che la modifica è stata apportata. Questo processo viene illustrato nella figura seguente.

![richiesta di modifica della password](images/pswdfilte.png)

La notifica di modifica della password viene usata per sincronizzare le modifiche delle password nei database di account esterni.

I filtri password vengono usati per applicare i criteri password. I filtri convalidano le nuove password e indicano se la nuova password è conforme ai criteri password implementati.

Per una panoramica dell'uso dei filtri password, vedere [Uso dei filtri password.](using-password-filters.md)

Per un elenco delle funzioni di filtro delle password, vedere [Funzioni di filtro password.](management-functions.md)

Negli argomenti seguenti vengono fornite ulteriori informazioni sui filtri password:

-   [Considerazioni sulla programmazione del filtro password](password-filter-programming-considerations.md)
-   [Imposizione e protezione delle password Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
