---
description: Fornisce informazioni specifiche di Schannel su un contesto di sicurezza.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Esecuzione di query degli attributi di un contesto Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f00f6d5f0660bbb3a0d4ce5890ab415325707dbda4087d025a010efdb3fd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919940"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Esecuzione di query degli attributi di un contesto Schannel

La [**funzione QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fornisce informazioni specifiche di Schannel su un [*contesto di sicurezza.*](../secgloss/s-gly.md) La maggior parte delle informazioni viene originariamente specificata quando il contesto viene creato usando la funzione [**Client InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) o server [**AcceptSecurityContext (Schannel).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Alcune informazioni vengono specificate quando si ottiene un handle per le credenziali usate per creare il contesto. Per altre informazioni, vedere [Recupero di credenziali Schannel](obtaining-schannel-credentials.md).

 

 
