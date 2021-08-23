---
description: In Windows Vista e versioni successive è possibile usare pseudo-impostazioni locali per testare la localizzabilità delle applicazioni. Questo argomento include le procedure per l'uso di pseudocodice.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Uso di pseudo-impostazioni locali per i test di localizzabilità
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: 72d84cbf324823a814c9412580b033792b0d1c8a45630bf2f4cb26dd8b2a1acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631721"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Uso di pseudo-impostazioni locali per i test di localizzabilità

[Le pseudo-impostazioni](pseudo-locales.md) locali sono incorporate per Windows Vista e versioni successive, in modo che sia possibile accedervi tramite le API NLS (National Language Support). È possibile usare pseudo-impostazioni locali per testare la [localizzabilità](/windows/uwp/design/globalizing/globalizing-portal) delle applicazioni. Questo argomento include le procedure per l'uso di pseudocodice.

> [!NOTE]
> Un'attività che richiede particolare attenzione quando si tratta di pseudo-impostazioni locali è enumerarle; nel codice o nella parte relativa alle opzioni internazionali e della lingua del Pannello di controllo. Altre informazioni più avanti in questo argomento.

I nomi delle pseudo-impostazioni locali sono "qps-ploc", "qps-ploca" e "qps-plocm". A Windows 10, sono disponibili anche le pseudo-impostazioni locali "qps-Latn-x-sh".

## <a name="retrieve-information-about-pseudo-locales"></a>Recuperare informazioni sulle pseudo-impostazioni locali

È possibile usare [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) per recuperare informazioni su una pseudo-impostazioni locali. Passare alla funzione il nome delle pseudo-impostazioni locali specifiche (vedere l'elenco di nomi sopra riportato). Ad esempio, "qps-plocm" per le pseudo-impostazioni locali con mirroring.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Usare LocaleNameToLCID con pseudo-impostazioni locali

È possibile chiamare la funzione di mapping NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) con il nome di una pseudo-impostazioni locali.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Abilitare le pseudo-impostazioni locali per l'enumerazione

Nell'applicazione è possibile chiamare [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) per enumerare le impostazioni locali riconoscite dal sistema. La parte relativa alle opzioni internazionali e di lingua del Pannello di controllo **chiama anche EnumSystemLocalesEx** per compilare l'elenco di impostazioni locali visualizzate. Tuttavia, per impostazione predefinita, le quattro pseudo-impostazioni locali elencate sopra non vengono riconosciute dal sistema, quindi non verranno restituite da **EnumSystemLocalesEx**. Per i sistemi da Windows Vista fino a Windows 10, versione 1709, la soluzione consiste nell'abilitare le pseudo-impostazioni locali aggiungendo chiavi al Registro Windows sistema.

Le modifiche vengono apportate nella chiave HKEY \_ LOCAL \_ MACHINE System \\ \\ CurrentControlSet \\ Control Nls per le lingue \\ installate nel sistema operativo. È possibile apportare queste impostazioni per abilitare le pseudo-impostazioni locali. Ogni chiave illustrata di seguito è l'LCID esadecimale corrispondente alle pseudo-impostazioni locali abilitate. Ogni valore è di tipo string (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

Ad Windows 10, versione 1803, la modifica del registro Windows come questo non ha alcun effetto. È comunque possibile chiamare le API NLS non enumerate con i nomi delle pseudo-impostazioni locali (vedere gli esempi di codice precedenti) per popolare l'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

* [Uso del supporto linguistico nazionale](using-national-language-support.md)
* [Pseudo-impostazioni locali](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
