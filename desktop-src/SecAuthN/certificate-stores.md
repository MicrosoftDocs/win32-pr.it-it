---
description: I certificati client e server devono essere archiviati in un archivio certificati accessibile dal processo dell'applicazione.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64451ea7f568bb5e86289d5d9f1587d98b65aa1d53c14a4a251a5e61fe72b21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883491"
---
# <a name="certificate-stores"></a>Archivi certificati

I [*certificati client*](/windows/desktop/SecGloss/c-gly) e [*server*](/windows/desktop/SecGloss/s-gly) devono essere archiviati in un archivio [*certificati*](/windows/desktop/SecGloss/c-gly) accessibile dal processo dell'applicazione. In genere, si tratta del Negozio personale, noto anche come archivio personale. Le applicazioni client come Internet Explorer in genere usano l'archivio My dell'utente corrente, mentre server come Internet Information Services (IIS) usano il sistema My store del computer locale.

L'archivio radice [](/windows/desktop/SecGloss/c-gly) e l'archivio autorità di certificazione (CA) vengono usati quando Schannel o un'applicazione compila una catena di certificati da inviare al computer remoto. Questi archivi vengono usati per convalidare una catena di certificati ricevuta. Per altre informazioni, vedere [Esecuzione dell'autenticazione tramite Schannel.](performing-authentication-using-schannel.md)

 

 
