---
description: Fornisce informazioni specifiche di SChannel su un contesto di sicurezza.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Esecuzione di query sugli attributi di un contesto Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128283"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Esecuzione di query sugli attributi di un contesto Schannel

La funzione [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fornisce informazioni specifiche di SChannel su un [*contesto di sicurezza*](../secgloss/s-gly.md). La maggior parte delle informazioni viene specificata in origine quando il contesto viene creato tramite la funzione client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) o server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Alcune informazioni vengono specificate quando si ottiene un handle per la credenziale utilizzata per creare il contesto. Per ulteriori informazioni, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md).

 

 
