---
title: Metodi della proprietà IADsNameTranslate (Iads.h)
description: Imposta la proprietà ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsNameTranslate ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3993c3f3680dca46d2f880705fae44812a3bb5fd7a046084c1d818c3433ea7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082385"
---
# <a name="iadsnametranslate-property-methods"></a>Metodi della proprietà IADsNameTranslate

Il metodo di proprietà [**dell'interfaccia IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) imposta la **proprietà ChaseReferral.** Per altre informazioni, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**InseguimentoReferral**
</dt> <dd> <dl>

Opzioni di ricerca dei riferimenti come definito in [**ADS \_ \_ REFERRALS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Quando è impostata la ricerca dei riferimenti, la conversione del nome viene eseguita su oggetti che non appartengono a questa directory e sono i riferimenti restituiti dalla ricerca dei riferimenti.

<dt>

Tipo di accesso: sola scrittura
</dt> <dt>

Tipo di dati di scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

Le opzioni di ricerca dei riferimenti si applicano solo quando si [**usa IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) e [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). La funzionalità non è disponibile con [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) o [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

[**L'interfaccia IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) ha un'implementazione parziale dell'enumerazione [**ADS \_ \_ REFERRALS REFERRALS \_ tramite**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) la **proprietà ReferralReferral.** Se la **proprietà ReferralReferral** è impostata su zero (0), corrisponde a specificare **ADS \_ \_ REFERRALS \_ NEVER** (0). Se viene usato un valore diverso da zero, corrisponde a specificare **ADS \_ \_ REFERRALS ALWAYS \_** (0x60). **IADsNameTranslate** non implementa le opzioni **ADS \_ REFERRAL \_ REFERRALS \_ SUBORDINATE** (0x20) o **ADS \_ REFERRAL \_ REFERRALS \_ EXTERNAL** (0x40).

L'impostazione predefinita per la ricerca dei riferimenti è abilitata (**ADS \_ \_ REFERRALS \_ ALWAYS**). Senza ricerca di riferimenti, è possibile eseguire la conversione dei nomi solo su tali oggetti che risiedono nel server di directory connesso. Se non si è incerti che l'oggetto di interesse si trova nel server specificato, è necessario impostare questa proprietà su **ADS \_ \_ REFERRALS \_ ALWAYS**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate è definito come B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ENUMERAZIONE ADS \_ \_ REFERRALS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Metodi delle proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





