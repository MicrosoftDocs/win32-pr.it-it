---
title: Tipi di dati dell'API del server HTTP versione 2.0
description: Tipi di dati dell'API del server HTTP versione 2.0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a347b58a97ad89e499136c07f85e18ee2ce1bddc31b5c6d67b8f14a2348a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950770"
---
# <a name="http-server-api-version-20-data-types"></a>Tipi di dati dell'API del server HTTP versione 2.0

L'API del server HTTP usa vari tipi di identificatore per scopi speciali dichiarati nell'intestazione Http.h come indicato di seguito:

-   **USHORT** HTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM, \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM
-   **ULONGLONG** ID \_ \_ OPACO HTTP, \* ID \_ OPACO PHTTP \_
-   **HTTP \_ ID \_ OPACO ID** \_ RICHIESTA \_ HTTP, ID RICHIESTA \* PHTTP \_ \_
-   **HTTP \_ ID \_ OPACO ID** CONNESSIONE \_ \_ HTTP, \* \_ ID CONNESSIONE PHTTP \_
-   **HTTP \_ ID \_ OPACO ID** CONNESSIONE HTTP \_ \_ \_ RAW, ID CONNESSIONE \* \_ PHTTP NON \_ \_ ELABORATO
-   **USHORT** HTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM, \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM

Un'applicazione non deve tentare di generare o modificare alcun identificatore appartenente a uno di questi tipi.

 

 




