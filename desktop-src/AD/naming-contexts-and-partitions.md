---
title: Contesti di denominazione e partizioni di directory
description: Ogni controller di dominio in una foresta di domini controllata da Active Directory Domain Services include le partizioni di directory.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Contesti di denominazione e partizioni di directory AD
- Contesti di denominazione AD, informazioni
- AD, informazioni sulle partizioni di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39934f0236e927bff281230c41a303f5e6d2bb0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956312"
---
# <a name="naming-contexts-and-directory-partitions"></a>Contesti di denominazione e partizioni di directory

Ogni controller di dominio in una foresta di domini controllata da Active Directory Domain Services include le [*partizioni di directory*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). Le partizioni di directory sono note anche come [*contesti di denominazione*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)). Una partizione di directory è una parte contigua della directory complessiva con ambito di replica indipendente e dati di pianificazione. Per impostazione predefinita, il servizio Dominio di Active Directory per un'azienda contiene le partizioni seguenti:

-   [*Partizione dello schema*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85)): la partizione dello schema contiene gli oggetti **classSchema** e **attributeSchema** che definiscono i tipi di oggetti che possono esistere nella foresta. Ogni controller di dominio nella foresta dispone di una replica della stessa partizione dello schema.
-   [*Partizione di configurazione*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85)): la partizione di configurazione contiene la topologia di replica e altri dati di configurazione che devono essere replicati in tutta la foresta. Ogni controller di dominio nella foresta dispone di una replica della stessa partizione di configurazione.
-   [*Partizione di dominio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)): la partizione di dominio contiene gli oggetti directory, ad esempio utenti e computer, associati al dominio locale. Un dominio può avere più controller di dominio e una foresta può avere più domini. Ogni controller di dominio archivia una replica completa della partizione di dominio per il dominio locale, ma non archivia le repliche delle partizioni di dominio per altri domini.

Windows Server 2003 introduce la *partizione di directory applicativa*, che consente di controllare l'ambito di replica e di consentire il posizionamento delle repliche in modo più appropriato per i dati dinamici. Per ulteriori informazioni sulle partizioni di directory applicative, vedere [informazioni sulle partizioni di directory applicative](about-application-directory-partitions.md).

Per ulteriori informazioni su come Active Directory Domain Services mantenere la coerenza tra le diverse repliche di una partizione di directory, vedere [replica e integrità dei dati](replication-and-data-integrity.md).

 

 