---
title: AuxUserType
description: Specifica il nome visualizzato breve di un'applicazione e i nomi delle applicazioni.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1dbec8e873e6f6cfcb5fdb29468c1f09c0a7a6935280054e129ddac0b49e282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550721"
---
# <a name="auxusertype"></a>AuxUserType

Specifica il nome visualizzato breve di un'applicazione e i nomi delle applicazioni.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Commenti

La lunghezza massima consigliata per *ShortDisplayName* è di 15 caratteri. Questo nome viene usato nei menu, inclusi i menu popup.

*ApplicationName* deve contenere il nome effettivo dell'applicazione, ad esempio "Acme Draw 2.0". Questo nome viene usato nel **campo Risultati** della finestra **di dialogo** Incolla speciale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




