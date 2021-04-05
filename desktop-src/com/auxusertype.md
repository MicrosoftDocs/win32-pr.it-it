---
title: AuxUserType
description: Specifica il nome visualizzato breve e i nomi delle applicazioni di un'applicazione.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707033"
---
# <a name="auxusertype"></a>AuxUserType

Specifica il nome visualizzato breve e i nomi delle applicazioni di un'applicazione.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Commenti

La lunghezza massima consigliata per *ShortDisplayName* è di 15 caratteri. Questo nome viene usato nei menu, inclusi i menu a comparsa.

*ApplicationName* deve contenere il nome effettivo dell'applicazione, ad esempio "Acme disegnato 2,0". Questo nome viene usato nel campo **risultati** della finestra di dialogo **Incolla speciale** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




