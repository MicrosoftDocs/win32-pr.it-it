---
title: Impostazione delle autorizzazioni per un gruppo di proprietà
description: Le autorizzazioni possono essere applicate a un gruppo di proprietà.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Impostazione delle autorizzazioni per un gruppo di proprietà AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724410"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>Impostazione delle autorizzazioni per un gruppo di proprietà

Le autorizzazioni possono essere applicate a un gruppo di proprietà. Un set di proprietà viene identificato dal GUID nell'attributo [**rightsGuid**](/windows/desktop/ADSchema/a-rightsguid) di un oggetto [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) . Questo GUID viene impostato nell'attributo [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) dell'oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) di ogni attributo del gruppo.

Nella procedura seguente viene illustrato come impostare le autorizzazioni che si applicano a un gruppo di proprietà dell'oggetto.

**Per impostare le autorizzazioni che si applicano a un gruppo di proprietà dell'oggetto**

1.  Impostare la proprietà [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ Rights \_ DS \_ Read \_ prop**, **Ads \_ Rights \_ DS \_ Write \_ prop** o entrambi i valori combinati.
2.  Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType accedere a \_ \_ \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.
3.  Impostare la proprietà [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul GUID del set di proprietà. Si tratta della proprietà [**rightsGuid**](/windows/desktop/ADSchema/a-rightsguid) dell'oggetto [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) che identifica il set di proprietà. Questo GUID viene inoltre impostato come [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) nell'oggetto attributeSchema di ogni proprietà del gruppo.
4.  Impostare la proprietà [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **tipo di \_ oggetto flag Ads \_ \_ \_ presente**.

Tenere presente che non è necessario impostare il flag di **\_ \_ \_ \_ accesso di controllo DS Rights ADS** nella proprietà [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) . Questo flag viene utilizzato solo per specificare un diritto di accesso del controllo.

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare i diritti di accesso per un set di proprietà, vedere [codice di esempio per l'impostazione delle autorizzazioni in un gruppo di proprietà](example-code-for-setting-permissions-on-a-group-of-properties.md).

Per ulteriori informazioni sulla creazione di una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE per un set di proprietà, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 