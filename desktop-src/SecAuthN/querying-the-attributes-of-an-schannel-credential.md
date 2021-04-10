---
description: Fornisce informazioni specifiche di SChannel su una credenziale.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Esecuzione di query sugli attributi di una credenziale Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227375"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a>Esecuzione di query sugli attributi di una credenziale Schannel

La funzione [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fornisce informazioni specifiche di SChannel su una credenziale. Queste informazioni vengono specificate in origine al momento della creazione della credenziale. Per ulteriori informazioni, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md). Le informazioni restituite da questa funzione sono valide per qualsiasi connessione ([*contesti di sicurezza*](../secgloss/s-gly.md)) creata utilizzando le credenziali specificate.

 

 
