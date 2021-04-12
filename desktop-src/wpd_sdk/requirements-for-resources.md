---
description: Requisiti per le risorse
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisiti per le risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232693"
---
# <a name="requirements-for-resources"></a>Requisiti per le risorse

I dispositivi portatili Windows definiscono le seguenti categorie di risorse come valori **PropertyKey** . Questi valori vengono utilizzati per descrivere le singole risorse in un oggetto. Il membro *PID* della chiave della proprietà può essere diverso per descrivere risorse diverse dello stesso tipo per tutti i tipi ad eccezione di **WPD \_ Resource \_ default**, che può descrivere solo una risorsa. La pagina di descrizione collegata per ogni tipo di risorsa elenca gli attributi supportati da tale risorsa.



| PROPERTYKEY risorse                                                | Descrizione                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md)              | Specifica l'intero file sottostante l'oggetto. Questa è l'unica risorsa necessaria per qualsiasi oggetto con una risorsa. |
| [**\_Art album delle risorse WPD \_ \_**](wpd-resource-album-art.md)         | Specifica un'immagine che rappresenta la grafica dell'album per l'oggetto.                                           |
| [**\_ \_ clip audio della risorsa WPD \_**](wpd-resource-audio-clip.md)       | Specifica un clip audio per l'oggetto.                                                                        |
| [**\_ \_ Foto contatto risorse \_ WPD**](wpd-resource-contact-photo.md) | Specifica un'immagine che rappresenta una foto dell'utente a cui si fa riferimento nell'oggetto contatto.                |
| [**\_risorsa WPD \_ generica**](wpd-resource-generic.md)              | Una risorsa generica del tipo di dati non definito. Questa operazione deve essere considerata come una matrice di byte.                             |
| [**\_icona della risorsa WPD \_**](wpd-resource-icon.md)                    | Un'icona.                                                                                                       |
| [**\_anteprima della risorsa WPD \_**](wpd-resource-thumbnail.md)          | Immagine di anteprima.                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



