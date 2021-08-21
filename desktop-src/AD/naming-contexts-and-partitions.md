---
title: Contesti dei nomi e partizioni di directory
description: Ogni controller di dominio in una foresta di dominio controllata da Active Directory Domain Services le partizioni di directory.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Contesti dei nomi e partizioni di directory AD
- Contesti dei nomi AD , Informazioni
- Partizioni di directory AD , Informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309b76b50270f093b3a4930680b343d517976e269e731082696b89bf6a58c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025709"
---
# <a name="naming-contexts-and-directory-partitions"></a>Contesti dei nomi e partizioni di directory

Ogni controller di dominio in una foresta di dominio controllata da Active Directory Domain Services le [*partizioni di directory*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). Le partizioni di directory sono note anche come [*contesti dei nomi*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)). Una partizione di directory è una parte contigua della directory complessiva con ambito di replica indipendente e dati di pianificazione. Per impostazione predefinita, il Dominio di Active Directory service per un'organizzazione contiene le partizioni seguenti:

-   [*Partizione dello*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85))schema: la partizione dello schema contiene gli **oggetti classSchema** e **attributeSchema** che definiscono i tipi di oggetti che possono esistere nella foresta. Ogni controller di dominio nella foresta ha una replica della stessa partizione dello schema.
-   [*Partizione di configurazione:*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85))la partizione di configurazione contiene la topologia di replica e altri dati di configurazione che devono essere replicati in tutta la foresta. Ogni controller di dominio nella foresta ha una replica della stessa partizione di configurazione.
-   [*Partizione di*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))dominio: la partizione di dominio contiene gli oggetti directory, ad esempio utenti e computer, associati al dominio locale. Un dominio può avere più controller di dominio e una foresta può avere più domini. Ogni controller di dominio archivia una replica completa della partizione di dominio per il dominio locale, ma non le repliche delle partizioni di dominio per altri domini.

Windows Server 2003 introduce la partizione di *directory* applicativa , che consente di controllare l'ambito della replica e di consentire il posizionamento delle repliche in modo più appropriato per i dati dinamici. Per altre informazioni sulle partizioni di directory applicative, vedere [Informazioni sulle partizioni di directory applicative](about-application-directory-partitions.md).

Per altre informazioni su come Active Directory Domain Services la coerenza tra le varie repliche di una partizione di directory, vedere [Replica e integrità dei dati](replication-and-data-integrity.md).

 

 