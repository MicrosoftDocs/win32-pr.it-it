---
title: ActivateAtStorage
description: Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato persistente utilizzato o da cui vengono inizializzati.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valore del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047450"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato persistente utilizzato o da cui vengono inizializzati.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** . Qualsiasi valore che inizia con ' Y ' o ' y ' indica che è necessario usare **ActivateAtStorage** .

La funzionalità **ActivateAtStorage** fornisce un modo trasparente per consentire ai client di individuare gli oggetti in esecuzione nello stesso computer dei dati utilizzati. In questo modo, il traffico di rete viene ridotto perché l'oggetto esegue chiamate a file system locali invece che chiamate attraverso la rete.

Quando viene impostato un valore per **ActivateAtStorage**, questo diventa il comportamento predefinito nelle chiamate alle funzioni [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) e all'implementazione del moniker di file di [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). In tutte queste chiamate, se si specifica una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , viene eseguito l'override dell'impostazione di **ActivateAtStorage** per la durata della chiamata di funzione. Il chiamante può passare le informazioni **COSERVERINFO** a **IMoniker:: BindToObject** tramite la struttura [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .

Il valore impostato per **ActivateAtStorage** è anche il comportamento predefinito quando \_ \_ viene specificato il server remoto CLSCTX se nel computer del client non sono installate informazioni sul Registro di sistema per la classe. Le applicazioni client scritte per sfruttare i vantaggi di **ActivateAtStorage** possono pertanto richiedere una minore amministrazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 