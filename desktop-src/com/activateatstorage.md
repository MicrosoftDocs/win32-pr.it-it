---
title: ActivateAtStorage
description: Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato permanente in uso o da cui vengono inizializzati.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valore del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8087313b8527ed95e7122d0e8dbe4fbd1ef028d7009f25937b3dc4300e9a4103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048899"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato permanente in uso o da cui vengono inizializzati.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ.** Qualsiasi valore che inizia con "Y" o "y" indica che è necessario **usare ActivateAtStorage.**

La **funzionalità ActivateAtStorage** offre un modo trasparente per consentire ai client di individuare gli oggetti in esecuzione nello stesso computer dei dati che usano. In questo modo si riduce il traffico di rete perché l'oggetto esegue chiamate al file system locale anziché chiamate in rete.

Quando un valore è impostato per **ActivateAtStorage,** questo diventa il comportamento predefinito nelle chiamate alle funzioni [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage,**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) nonché all'implementazione del moniker di file [**di IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). In tutte queste chiamate, specificando una [**struttura COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) viene eseguito l'override dell'impostazione **di ActivateAtStorage** per la durata della chiamata di funzione. Il chiamante può **passare informazioni COSERVERINFO** **a IMoniker::BindToObject** tramite la [**struttura BIND \_ OPTS2.**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)

Il valore impostato per **ActivateAtStorage** è anche il comportamento predefinito quando si specifica CLSCTX REMOTE SERVER se nel computer client non è installata alcuna informazione del Registro \_ di sistema per la \_ classe. Le applicazioni client scritte per sfruttare **i vantaggi di ActivateAtStorage** possono quindi richiedere una minore amministrazione.

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

[**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> </dl>

 

 