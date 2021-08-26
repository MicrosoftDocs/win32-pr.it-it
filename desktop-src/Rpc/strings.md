---
title: Attributo string (RPC)
description: L'attributo \ string\ e RPC (Remote Procedure Call).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58b0750169a89f34840333f1ea55ee2ee096b24f3b87e425035f04ca759849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127701"
---
# <a name="string-attribute-rpc"></a>Attributo string (RPC)

L'attributo stringa indica che il parametro è un puntatore a una matrice di \[ [](/windows/desktop/Midl/string) \] tipo [char](/windows/desktop/Midl/char-idl), [byte](/windows/desktop/Midl/byte)o **w \_ char**. Come per una matrice conforme, le dimensioni di un parametro **\[ stringa \]** vengono determinate in fase di esecuzione. A differenza di una matrice conforme, **\[ \]** lo sviluppatore non deve fornire la lunghezza associata alla matrice. L'attributo stringa indica allo stub di determinare le dimensioni della matrice chiamando **strlen**. Non **\[ è \]** possibile usare un attributo stringa contemporaneamente a \[ [quanto la lunghezza \_ è o](/windows/desktop/Midl/length-is) \] \[ [l'ultima è \_ .](/windows/desktop/Midl/last-is) \]

La **\[ combinazione \] di attributi** stringa in indica al stub di passare la stringa solo dal client al server. La quantità di memoria allocata nel server è uguale alla dimensione della stringa trasmessa più una.

Gli \[ [attributi out](/windows/desktop/Midl/out-idl), **string** \] indirizzano lo stub al passaggio della stringa solo dal server al client. La progettazione della chiamata per valore del linguaggio C afferma che tutti i **\[ parametri out \]** devono essere puntatori.

Il **\[ parametro out \]** deve essere un puntatore e, per impostazione predefinita, tutti i parametri del puntatore sono puntatori di riferimento. Il puntatore di riferimento non cambia durante la chiamata, ma punta alla stessa memoria di prima della chiamata. Per i puntatori di stringa, il vincolo aggiuntivo del puntatore di riferimento indica che il client deve allocare memoria valida sufficiente prima di effettuare la chiamata di procedura remota. Gli stub trasmettono la stringa **\[ che gli attributi \] di** stringa out indicano nella memoria già allocata sul lato client.

Negli argomenti seguenti vengono descritti i prototipi dei parametri di procedura remota per le stringhe:

-   [\[in, out, string \] Prototype](-in-out-string-prototype.md)
-   [\[in, string \] e \[ out, string \] Prototype](-in-string-and-out-string-prototype.md)

 

 