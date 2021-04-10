---
description: I certificati X.509 versione 3 contengono i campi di base definiti nelle versioni 1 e 2 più le estensioni di certificato. Nell'esempio seguente viene illustrata la sintassi ASN. 1 delle estensioni del certificato.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Estensioni versione 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231503"
---
# <a name="version-3-extensions"></a>Estensioni versione 3

I certificati X.509 versione 3 contengono i campi di base definiti nelle versioni 1 e 2 più le estensioni di certificato. Nell'esempio seguente viene illustrata la sintassi ASN. 1 delle estensioni del certificato.

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

Nella tabella seguente sono elencate le estensioni standard della versione 3 e i relativi identificatori di oggetto (OID). Microsoft supporta questi e include estensioni personalizzate aggiuntive. Per ulteriori informazioni, vedere [estensioni](extensions.md).

| Estensione                                         | Descrizione                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificatore di chiave dell'autorità (2.5.29.19)<br/>    | Identifica la chiave pubblica dell'autorità di certificazione corrispondente alla chiave privata dell'autorità usata per firmare il certificato.                                                                              |
| Vincoli di base (2.5.29.35)<br/>           | Specifica se l'entità può essere usata come autorità di certificazione e, in caso affermativo, il numero di autorità di certificazione subordinate che possono esistere nella catena di certificati.                                                           |
| Criteri certificati (2.5.29.32)<br/>        | Specifica i criteri in base ai quali il certificato è stato rilasciato e gli scopi per cui può essere usato.                                                                                            |
| Punti di distribuzione CRL (2.5.29.31)<br/>     | Contiene l'URI dell'elenco di [*revoche di certificati*](/windows/desktop/SecGloss/c-gly) (CRL) di base.                                  |
| Utilizzo chiavi avanzato (2.5.29.46)<br/>          | Specifica il modo in cui è possibile usare la chiave pubblica contenuta nel certificato.                                                                                                                   |
| Nome alternativo autorità emittente (2.5.29.8)<br/>      | Specifica una o più forme di denominazione alternative per l'autorità di certificazione della richiesta di certificato.                                                                                                                  |
| Utilizzo chiave (2.5.29.15)<br/>                   | Specifica le restrizioni relative alle operazioni eseguibili dalla chiave pubblica contenuta nel certificato.                                                                                           |
| Vincoli di nome (2.5.29.30)<br/>            | Specifica lo spazio dei nomi all'interno del quale devono trovarsi tutti i nomi del soggetto in una gerarchia di certificati. L'estensione è usata solo in un certificato di autorità di certificazione.                                                       |
| Vincoli dei criteri (2.5.29.36)<br/>          | Vincola la convalida del percorso vietando il mapping dei criteri o richiedendo che ogni certificato nella gerarchia contenga un identificatore di criteri accettabile. L'estensione è usata solo in un certificato di autorità di certificazione. |
| Mapping dei criteri (2.5.29.33)<br/>             | Specifica i criteri in un'autorità di certificazione subordinata corrispondenti ai criteri dell'autorità di certificazione emittente.                                                                                                                |
| Periodo di utilizzo chiave privata (2.5.29.16)<br/>    | Specifica un periodo di validità per la chiave privata diverso da quello del certificato a cui la chiave è associata.                                                                             |
| Nome alternativo del soggetto (2.5.29.17)<br/>    | Specifica una o più forme di denominazione alternative per il soggetto della richiesta di certificato. Esempi di forme alternative includono indirizzi email, nomi DNS; indirizzi IP e URI.                           |
| Attributi di directory soggetto (2.5.29.9)<br/> | Trasmette gli attributi di identificazione, ad esempio la nazionalità, del soggetto del certificato. Il valore dell'estensione è una sequenza di coppie di valori OID.                                                              |
| Identificatore di chiave del soggetto (2.5.29.14)<br/>      | Distingue tra più chiavi pubbliche detenute dal soggetto del certificato. Il valore dell'estensione è in genere un hash SHA-1 della chiave.                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Campi di base](about-basic-fields.md)
</dt> <dt>

[Campi versione 2](about-version-2-fields.md)
</dt> <dt>

[Certificati di chiave pubblica X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

