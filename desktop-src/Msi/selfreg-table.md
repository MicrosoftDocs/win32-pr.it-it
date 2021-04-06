---
description: La tabella SelfReg contiene informazioni sui moduli che devono essere registrati autonomamente.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabella SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760145"
---
# <a name="selfreg-table"></a>Tabella SelfReg

La tabella SelfReg contiene informazioni sui moduli che devono essere registrati autonomamente. Il programma di installazione chiama la funzione [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante l'installazione del modulo. chiama [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante la disinstallazione del modulo. Il programma di installazione non registra autonomamente i file EXE.

La tabella SelfReg include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| file\_ | [Identificatore](identifier.md) | S   | N        |
| Costo   | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella file](file-table.md) che indica il modulo che deve essere registrato.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo
</dt> <dd>

Costo della registrazione del modulo in byte. Deve essere un numero non negativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli autori dei pacchetti di installazione si sconsigliano vivamente di usare la registrazione automatica. Devono invece registrare i moduli creando una o più tabelle fornite dal programma di installazione per questo scopo. Per ulteriori informazioni, vedere [gruppo di tabelle del registro di sistema](registry-tables-group.md). Molti dei vantaggi derivanti dalla presenza di un servizio di installazione centrale vengono persi con la registrazione automatica perché le routine di registrazione automatica tendono a nascondere le informazioni di configurazione critiche. I motivi per evitare la registrazione automatica includono:

-   Il rollback di un'installazione con moduli autoregistrati non può essere eseguito in modo sicuro con [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) perché non esiste alcun modo per stabilire se le chiavi autoregistrate vengono usate da un'altra funzionalità o applicazione.
-   La possibilità di usare l'annuncio è ridotta se la registrazione di classi o server di estensione viene eseguita in routine di registrazione automatica.
-   Il programma di installazione gestisce automaticamente le chiavi di HKCR nelle tabelle del registro di sistema per le installazioni per utente o per computer. Le routine [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) attualmente non supportano la nozione di chiave HKCR per utente.
-   Se più utenti usano un'applicazione autoregistrata nello stesso computer, ogni utente deve installare l'applicazione la prima volta che la esegue. In caso contrario, il programma di installazione non è in grado di determinare facilmente le chiavi di registro HKCU appropriate
-   A [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) è possibile negare l'accesso alle risorse di rete, ad esempio le librerie dei tipi, se un componente viene specificato come Run-from-source ed è elencato nella tabella SelfReg. Questa operazione può causare un errore di installazione del componente durante un'installazione amministrativa.
-   La registrazione automatica delle dll è più soggetta a errori di codifica perché il nuovo codice necessario per [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) è generalmente diverso per ogni dll. Usare invece le tabelle del registro di sistema nel database per sfruttare il codice esistente fornito dal programma di installazione.
-   La registrazione automatica delle dll può talvolta essere collegata a DLL ausiliarie che non sono presenti o sono la versione sbagliata. Al contrario, il programma di installazione può registrare le dll utilizzando le tabelle del registro di sistema senza dipendenze dallo stato corrente del sistema.

> [!Note]  
> Non è possibile specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione delle dll con registrazione automatica usando le azioni [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) . Vedere [specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md).

 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
