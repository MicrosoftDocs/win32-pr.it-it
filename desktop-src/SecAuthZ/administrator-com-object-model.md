---
description: Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto Component Object Model con privilegi elevati.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modello a oggetti COM administrator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b331d71f83428ad821bc1c2f9de24984025aaf7f95874c2203ee9fb1f9158a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784788"
---
# <a name="administrator-com-object-model"></a>Modello a oggetti COM administrator

Nel modello a oggetti COM dell'amministratore, un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto Component Object Model [con](/windows/desktop/com/component-object-model--com--portal) privilegi elevati. Per informazioni sulla creazione di un oggetto COM con privilegi elevati, vedere [Moniker di elevazione dei privilegi COM.](../com/the-com-elevation-moniker.md)

Uno svantaggio dell'uso del modello a oggetti COM dell'amministratore è che all'utente viene richiesto ogni volta che viene eseguita un'operazione con privilegi.

Qualsiasi interfaccia utente in grado di controllare l'oggetto COM deve essere presentata dall'oggetto COM stesso. In caso contrario, un processo senza privilegi potrebbe causare l'esecuzione di operazioni con privilegi da parte dell'oggetto COM con privilegi senza che venga richiesto all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello broker amministratore](administrator-broker-model.md)
</dt> <dt>

[Modello di attività con privilegi elevati](elevated-task-model.md)
</dt> <dt>

[Modello di servizio del sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
