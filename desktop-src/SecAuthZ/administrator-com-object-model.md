---
description: Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto Component Object Model con privilegi elevati.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modello a oggetti COM dell'amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883869"
---
# <a name="administrator-com-object-model"></a>Modello a oggetti COM dell'amministratore

Nel modello a oggetti COM dell'amministratore, un'applicazione eseguita come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto [Component Object Model](/windows/desktop/com/component-object-model--com--portal) con privilegi elevati. Per informazioni sulla creazione di un oggetto COM con privilegi elevati, vedere [il moniker di elevazione com](../com/the-com-elevation-moniker.md).

Uno svantaggio dell'utilizzo del modello a oggetti COM dell'amministratore è che l'utente viene richiesto ogni volta che viene eseguita un'operazione con privilegi.

Qualsiasi interfaccia utente in grado di controllare l'oggetto COM deve essere presentata dall'oggetto COM stesso. In caso contrario, un processo senza privilegi può causare l'esecuzione di operazioni privilegiate da parte dell'oggetto COM con privilegi elevati senza che venga richiesto all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni che richiedono privilegi di amministratore](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modello di broker amministratore](administrator-broker-model.md)
</dt> <dt>

[Modello di attività con privilegi elevati](elevated-task-model.md)
</dt> <dt>

[Modello di servizio del sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
