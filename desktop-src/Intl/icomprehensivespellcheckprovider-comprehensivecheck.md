---
description: Eseguire il controllo ortografico del testo del provider in modo più accurato rispetto a ISpellCheckProvider::Check.
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: Metodo IComprehensiveSpellCheckProvider::ComprehensiveCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: ee1b07eb2f459aca3955b0a1c5ad2e2e2139cc196f618430b3039b1eba1e3971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086601"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>Metodo IComprehensiveSpellCheckProvider::ComprehensiveCheck

Eseguire il controllo ortografico del testo del provider in modo più accurato rispetto a [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*text* \[ Pollici\]
</dt> <dd>

Testo da controllare.

</dd> <dt>

*result* \[ Cambio\]
</dt> <dd>

Risultato del controllo di questo testo, come enumerazione di errori di ortografia ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), se presenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore restituito                                                                             | Descrizione                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>         | Successo.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | *text* è una stringa vuota.<br/> |
| <dl> <dt>PUNTATORE E \_</dt> </dl>    | *text* è un puntatore Null.<br/>  |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata da un provider di controllo ortografico. Tuttavia, se il provider supporta due "modalità" di controllo ortografico (una più veloce e una più lenta ma più completa), deve implementare questa interfaccia nello stesso oggetto che implementa [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) per supportare la modalità di controllo più approfondita. Quando un client chiama [**ISpellChecker::ComprehensiveCheck,**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)la funzionalità di controllo ortografico esegue [**queryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul provider [**per IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)e chiama **IComprehensiveSpellCheckProvider.ComprehensiveCheck** se l'interfaccia è supportata. Se l'interfaccia non è supportata, il fall-back verrà automaticamente verso [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
