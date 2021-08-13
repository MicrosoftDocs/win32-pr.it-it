---
description: La tabella SelfReg contiene informazioni sui moduli che devono essere registrati automaticamente.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabella SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d00b9f18755cf3284edfd1ba9476b12ba6343c816dbafe84ac3c3676f663f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625507"
---
# <a name="selfreg-table"></a>Tabella SelfReg

La tabella SelfReg contiene informazioni sui moduli che devono essere registrati automaticamente. Il programma di installazione chiama [**la funzione DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante l'installazione del modulo. chiama [**DllUnregisterServer durante**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) la disinstallazione del modulo. Il programma di installazione non registra automaticamente i file EXE.

La tabella SelfReg contiene le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| file\_ | [Identificatore](identifier.md) | S   | N        |
| Cost   | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [File che](file-table.md) indica il modulo che deve essere registrato.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo
</dt> <dd>

Costo della registrazione del modulo in byte. Deve essere un numero non negativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli autori di pacchetti di installazione sono fortemente sconsigliati di usare la registrazione automatica. Devono invece registrare i moduli mediante la creazione di una o più tabelle fornite dal programma di installazione a questo scopo. Per altre informazioni, vedere [Gruppo di tabelle del Registro di sistema.](registry-tables-group.md) Molti dei vantaggi derivanti dalla presenza di un servizio di installazione centrale vengono persi con la registrazione automatica perché le routine di registrazione automatica tendono a nascondere informazioni di configurazione critiche. I motivi per evitare la registrazione automatica includono:

-   Il rollback di un'installazione con moduli autoregistrato non può essere eseguito in modo sicuro usando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) perché non è possibile determinare se le chiavi autoregistrato vengono usate da un'altra funzionalità o applicazione.
-   La possibilità di usare l'annuncio viene ridotta se la registrazione del server della classe o dell'estensione viene eseguita all'interno di routine di auto-registrazione.
-   Il programma di installazione gestisce automaticamente le chiavi HKCR nelle tabelle del Registro di sistema per le installazioni per utente o per computer. Le routine [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) attualmente non supportano la nozione di chiave HKCR per utente.
-   Se più utenti usano un'applicazione auto-registrata nello stesso computer, ogni utente deve installare l'applicazione la prima volta che la esegue. In caso contrario, il programma di installazione non è in grado di determinare facilmente l'esistenza delle chiavi del Registro di sistema HKCU appropriate.
-   A [**DllRegisterServer può**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) essere negato l'accesso alle risorse di rete, ad esempio le librerie dei tipi, se un componente è specificato come run-from-source ed è elencato nella tabella SelfReg. Ciò può causare l'esito negativo dell'installazione del componente durante un'installazione amministrativa.
-   Le DLL con registrazione autonoma sono più soggette a errori di codifica perché il nuovo codice necessario per [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) è in genere diverso per ogni DLL. Usare invece le tabelle del Registro di sistema nel database per sfruttare il codice esistente fornito dal programma di installazione.
-   Le DLL con registrazione autonoma possono talvolta essere collegate a DLL ausiliarie che non sono presenti o sono la versione errata. Al contrario, il programma di installazione può registrare le DLL usando le tabelle del Registro di sistema senza alcuna dipendenza dallo stato corrente del sistema.

> [!Note]  
> Non è possibile specificare l'ordine in cui il programma di installazione registra o annulla la registrazione delle DLL con registrazione automatica usando le azioni [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules.](selfunregmodules-action.md) Vedere [Specifica dell'ordine di registrazione automatica.](specifying-the-order-of-self-registration.md)

 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
