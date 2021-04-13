---
title: Glossario di accesso ai dispositivi
description: Di seguito sono riportati i termini usati in tutta la documentazione per l'API di accesso ai dispositivi.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398524"
---
# <a name="device-access-glossary"></a>Glossario di accesso ai dispositivi

Di seguito sono riportati i termini usati in tutta la documentazione per l'API di accesso ai dispositivi.

<dl> <dt>

**AppContainer**
</dt> <dd>

Ambiente di esecuzione altamente limitato in cui un processo viene eseguito con un subset ridotto dei privilegi dell'utente. Un processo in esecuzione all'interno di un AppContainer viene chiamato processo AppContainer. Un processo AppContainer è isolato dagli altri processi AppContainer e dal profilo dell'utente. Ha accesso limitato a un piccolo subset di risorse di sistema, ad esempio file, dispositivi, chiavi del registro di sistema, IPC (Interprocess Communication) endpoint di chiamata di procedura/remote (RPC) e risorse di rete.

</dd> <dt>

**Associazione**
</dt> <dd>

Associazione di un oggetto di accesso al dispositivo a una particolare interfaccia del dispositivo. Se l'associazione ha esito positivo, le app di Windows Store possono usare l'oggetto accesso al dispositivo come broker per comunicare con il driver di dispositivo.

</dd> <dt>

**Gestore**
</dt> <dd>

Componente che fornisce l'accesso a una risorsa che non viene concessa per impostazione predefinita.

</dd> <dt>

**App con privilegi**
</dt> <dd>

App identificata nei metadati di un determinato dispositivo come associato a tale dispositivo, in modo che possa comunicare con l'interfaccia limitata del driver di dispositivo. Un esempio di un'app di questo tipo potrebbe essere un'app per la riproduzione di musica proprietaria che dispone di autorizzazioni esclusive per la sincronizzazione con un lettore musicale portatile, quando le app dei concorrenti non possono. Per altre informazioni su come impostare i metadati di un dispositivo o su come limitare un driver alle app con privilegi, vedere [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).

</dd> </dl>
