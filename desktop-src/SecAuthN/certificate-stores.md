---
description: I certificati client e server devono essere archiviati in un archivio certificati accessibile dal processo dell'applicazione.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049769"
---
# <a name="certificate-stores"></a>Archivi certificati

I certificati [*client*](/windows/desktop/SecGloss/c-gly) e [*Server*](/windows/desktop/SecGloss/s-gly) devono essere archiviati in un [*archivio certificati*](/windows/desktop/SecGloss/c-gly) accessibile dal processo dell'applicazione. In genere, si tratta dell'archivio My, noto anche come archivio personale. Le applicazioni client, ad esempio Internet Explorer, utilizzano in genere l'archivio personale dell'utente corrente, mentre i server come Internet Information Services (IIS) utilizzano il sistema My Store del computer locale.

L'archivio radice e l'archivio [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA) vengono usati quando Schannel o un'applicazione compila una catena di certificati da inviare al computer remoto. Questi archivi vengono usati per convalidare una catena di certificati ricevuta. Per altre informazioni, vedere [esecuzione dell'autenticazione con Schannel](performing-authentication-using-schannel.md).

 

 
